<template>
  <v-app-bar
    ref="appBar"
    app
    dense
    color="#6A76AB"
    dark
    shrink-on-scroll
    prominent
    :src="require('../assets/starry-903-1920x180.jpg')"
    fade-img-on-scroll
    scroll-threshold="400"
  >
    <template v-slot:img="{ props }">
      <v-img
        v-bind="props"
        gradient="to top right, rgba(100,115,201,.7), rgba(25,32,72,.7)"
      ></v-img>
    </template>
    <!-- src="https://picsum.photos/1920/1080?random" -->
    <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

    <v-toolbar-title class="perceive">
      <router-link to="/" tag="span" style="cursor: pointer">
        <v-img
          ref="logoRef"
          :src="require('../assets/running-100.png')"
          class="logo"
        ></v-img>
      </router-link>
    </v-toolbar-title>

    <div class="flex-grow-1"></div>

    <!-- <v-text-field
        v-model="searchText"
        prepend-icon="mdi-plus"
        solo
        append-icon="mdi-magnify"
        hide-details
        single-line
      ></v-text-field> -->

    <div class="search perceive">
      <v-select
        :items="['课程', '作品']"
        placeholder="课程"
        class="pattern"
      ></v-select>
      <v-text-field>
        <v-icon slot="append">
          mdi-magnify
        </v-icon>
        <slot></slot>
        <!-- <v-icon slot="prepend" color="green">
          mdi-minus
        </v-icon> -->
        <!-- <v-select
          slot="prepend"
          :items="['关键字', '分类']"
          label="关键字"
          outlined
        ></v-select> -->
      </v-text-field>
    </div>

    <!-- <v-spacer /> -->
    <v-btn icon class="perceive">
      <v-icon>mdi-apps</v-icon>
    </v-btn>
    <v-btn icon class="perceive">
      <v-icon>mdi-bell</v-icon>
    </v-btn>
    <v-btn icon large class="perceive">
      <v-avatar size="32px" item>
        <v-icon>mdi-account-circle</v-icon>
      </v-avatar>
    </v-btn>

    <template v-if="isHome" v-slot:extension>
      <v-tabs
        ref="navTabsRef"
        align-with-title
        background-color="transparent"
        :class="{ nav: true }"
        active-class="nav-actived"
        @change="onChange($event)"
      >
        <v-tab class="nav-menu">首页</v-tab>
        <v-tab class="nav-menu">作品</v-tab>
        <v-tab class="nav-menu">课程</v-tab>
        <v-tab class="nav-menu">分享</v-tab>
        <v-tab class="nav-menu">交流</v-tab>
        <v-tab-item class="nav-item"></v-tab-item>
        <v-tab-item class="nav-item"></v-tab-item>
        <v-tab-item class="nav-item">
          <Category />
        </v-tab-item>
        <v-tab-item class="nav-item"></v-tab-item>
        <v-tab-item class="nav-item"></v-tab-item>
      </v-tabs>
    </template>
  </v-app-bar>
</template>

<script>
import Category from '@/components/Category'
export default {
  components: {
    Category
  },
  data() {
    return {
      height: 128,
      tab: null,
      navActived: 'nav-actived',
      navPosition: 0,
      isVertical: false,
      isHome: false
    }
  },
  computed: {},
  mounted() {
    this.isVertical = !this.$route.path.startsWith('/search')
    this.isHome = this.$route.path === '/'
    this.$watch(
      () => {
        return this.$refs.appBar.styles.height
      },
      (val) => {
        this.height = parseInt(val.substring(0, val.length - 2))
        this.$refs.logoRef.$el.style.transform = `scale(${this.height /
          192}) translate(0, ${this.height / 20}%)`
        // this.$refs.logoRef.styles.transform = `scale(${this.height / 100})`
      }
    )
  },
  methods: {
    onChange(index) {
      if (this.isVertical && this.$refs.navTabsRef) {
        // 42为tab margin-left
        this.navPosition = 42 + index * (16 * 2 + 58)
        // eslint-disable-next-line prettier/prettier
        const activedNavTabItem = this.$refs.navTabsRef.$children[1]
        activedNavTabItem.$el.style.left = this.navPosition + 'px'
      }
    }
  }
}
</script>

<style lang="scss" scope>
@media only screen and (max-width: 959px) {
  .perceive {
    align-content: center;
    margin: auto !important;
  }
}
.perceive {
  margin: auto !important;
}

.search {
  display: flex;
  margin: 48px 0;
  .pattern {
    .v-input__control {
      .v-input__slot:before,
      .v-input__slot:after {
        border-style: none;
      }
    }
    .v-select__selections {
      width: 30px;
    }
  }
}
.v-text-field__details {
  display: none;
}
body {
  background-color: #fafafa;
}
.v-select-list {
  background-color: transparent !important;
  color: white;
  .v-list {
    background-color: transparent !important;
    color: white;
  }
  .v-list-item {
    color: white !important;
  }
}

.theme--light.v-list-item:not(.v-list-item--active):not(.v-list-item--disabled) {
  color: white !important;
}
.nav {
  .v-item-group {
    width: fit-content;
  }
  .nav-item {
    color: #333;
    font-size: 18px;
    // margin-bottom: -10px;
  }
  .nav-menu {
    font-size: 24px;
  }
}
.v-tabs-slider {
  background-color: chocolate !important;
}

.nav-actived {
  // color: chocolate !important;
  // background-color: white !important;
  // opacity: 1 !important;

  // i.subtitle-icon {
  //   color: var(--v-primary-darken1);
  // }
}

.category {
  .v-tab--active {
    color: orangered;
  }
}

.category-end {
  max-width: 360px;
  color: #333;
  font-size: 18px;
}
.category-second {
  .v-slide-group__wrapper {
    border-right: 1px dashed #eee !important;
  }
}

.horizontal {
  [role='tablist'] {
    height: 48px !important;
  }
  .category-end {
    max-width: 100%;
  }
  // .nav .v-item-group {
  //   width: 100% !important;
  // }
}
.nav.horizontal {
  .v-item-group {
    width: 100% !important;
  }
  // .nav-item {
  //   color: #333;
  //   font-size: 18px;
  //   // margin-bottom: -10px;
  // }
  // .v-tabs-slider {
  //   background-color: chocolate !important;
  // }
}
</style>
