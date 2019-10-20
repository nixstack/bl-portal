<template>
  <v-card>
    <v-tabs
      :vertical="isVertical"
      :style="{ left: navPosition }"
      :class="{ category: true, horizontal: !isVertical }"
      center-active
      show-arrows
    >
      <v-tab>
        计算机图形
      </v-tab>
      <v-tab-item>
        <v-card>
          <v-tabs
            :vertical="isVertical"
            class="category-second"
            center-active
            show-arrows
          >
            <v-tab>原画设计</v-tab>
            <v-tab>三维建模</v-tab>
            <v-tab>材质/贴图</v-tab>
            <v-tab>灯光/渲染</v-tab>
            <v-tab>绑定/动画</v-tab>
            <v-tab>脚本/特效</v-tab>
            <v-tab>环境艺术</v-tab>
            <v-tab>影视制作</v-tab>
            <v-tab>3&nbsp;D&nbsp;打印</v-tab>
            <v-tab-item>
              <v-container class="category-end">
                <v-row>
                  <v-col>
                    <v-row>
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink
                          :to="{ name: 'search', params: { id: '.id' } }"
                          >绘画基础</NuxtLink
                        ></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="search">鼠绘</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">手绘</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">场景</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">概念</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">人物</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">卡通</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">日系</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">古风</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">国漫</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">日系</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">古风</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">国漫</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">日系</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">古风</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">国漫</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">日系</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">古风</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">国漫</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">日系</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">古风</NuxtLink></v-sheet
                      >
                      <v-sheet class="ma-3 px-1" elevation="3"
                        ><NuxtLink to="/search">国漫</NuxtLink></v-sheet
                      >
                    </v-row>
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
            <v-tab-item>
              <v-container class="category-end">
                <v-row>
                  <v-col>
                    <v-row>
                      <v-sheet class="ma-3 px-1" elevation="3">角色</v-sheet>
                      <v-sheet class="ma-3 px-1" elevation="3">场景</v-sheet>
                      <v-sheet class="ma-3 px-1" elevation="3">硬表面</v-sheet>
                      <v-sheet class="ma-3 px-1" elevation="3">生物</v-sheet>
                      <v-sheet class="ma-3 px-1" elevation="3">异形</v-sheet>
                      <v-sheet class="ma-3 px-1" elevation="3">概念</v-sheet>
                      <v-sheet class="ma-3 px-1" elevation="3">植被</v-sheet>
                      <v-sheet class="ma-3 px-1" elevation="3">地形</v-sheet>
                      <v-sheet class="ma-3 px-1" elevation="3">机械</v-sheet>
                    </v-row>
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
          </v-tabs>
        </v-card>
      </v-tab-item>
    </v-tabs></v-card
  >
</template>

<script>
export default {
  data() {
    return {
      navPosition: null,
      isVertical: false
    }
  },
  mounted() {
    this.isVertical = !this.$route.path.startsWith('/search')
  }
}
</script>

<style lang="scss" scoped>
// .category-second {
//   max-height: 500px;
// }
</style>
