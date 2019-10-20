<template>
  <div>
    <v-carousel class="full-width" cycle>
      <v-carousel-item v-for="(item, i) in carousels" :key="i">
        <v-sheet height="100%" tile>
          <v-row class="fill-height" align="center" justify="center">
            <div class="display-3">
              <v-img :src="item">
                <!-- <v-card-title class="card-title"
                  >原画、建模、动画、特效、影视后期</v-card-title
                > -->
              </v-img>
            </div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <v-container>
      <v-row>
        <v-col cols="12">
          <v-expansion-panels>
            <v-expansion-panel>
              <v-expansion-panel-header>
                <!-- <v-card
                    v-for="n in 5"
                    :key="n"
                    class="ma-3 mx-auto"
                    max-width="300"
                    raised
                  >
                    <v-img :src="require('../assets/ocean-280x100.jpg')">
                    </v-img>
                  </v-card> -->
                <v-row dense>
                  <v-card
                    v-for="(item, i) in softwares1"
                    :key="i"
                    class="ma-3 mx-auto"
                  >
                    <div
                      class="d-flex flex-no-wrap justify-space-between card-software"
                    >
                      <div>
                        <v-card-title
                          class="headline"
                          v-text="item.title"
                        ></v-card-title>
                        <div class="v-card-subtitle" v-text="item.artist"></div>
                        <!-- <v-card-subtitle v-text="item.artist"></v-card-subtitle> -->
                      </div>

                      <v-avatar class="ma-3" size="80" tile>
                        <v-img :src="item.src"></v-img>
                      </v-avatar>
                    </div>
                  </v-card>
                </v-row>

                <template v-slot:actions>
                  <span class="software">软件专题</span>
                  <v-icon color="orange">mdi-chevron-down</v-icon>
                </template></v-expansion-panel-header
              >
              <v-expansion-panel-content>
                <v-row dense>
                  <v-card
                    v-for="(item, i) in softwares2"
                    :key="i"
                    class="ma-3 mx-auto"
                  >
                    <div
                      class="d-flex flex-no-wrap justify-space-between card-software"
                    >
                      <div>
                        <v-card-title
                          class="headline"
                          v-text="item.title"
                        ></v-card-title>
                        <div class="v-card-subtitle" v-text="item.artist"></div>
                        <!-- <v-card-subtitle v-text="item.artist"></v-card-subtitle> -->
                      </div>

                      <v-avatar class="ma-3" size="80" tile>
                        <v-img :src="item.src"></v-img>
                      </v-avatar>
                    </div>
                  </v-card>
                </v-row>
                <v-row dense>
                  <v-card
                    v-for="(item, i) in softwares2"
                    :key="i"
                    class="ma-3 mx-auto"
                  >
                    <div
                      class="d-flex flex-no-wrap justify-space-between card-software"
                    >
                      <div>
                        <v-card-title
                          class="headline"
                          v-text="item.title"
                        ></v-card-title>
                        <div class="v-card-subtitle" v-text="item.artist"></div>
                        <!-- <v-card-subtitle v-text="item.artist"></v-card-subtitle> -->
                      </div>

                      <v-avatar class="ma-3" size="80" tile>
                        <v-img :src="item.src"></v-img>
                      </v-avatar>
                    </div>
                  </v-card>
                </v-row>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <v-row class="skill_title" justify="space-between">
            <div class="skill_title--main">精品推荐</div>
            <div class="more">更多>></div>
          </v-row>
          <v-row justify="center">
            <v-col cols="6">
              <div class="skill_desc">
                大数据时代，根据行业行情和发展趋势以及浏览和点赞人数分析，优质资源推荐，用数据说话，我们只做行业的口碑！
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-card
              v-for="n in 4"
              :key="n"
              class="ma-3 mx-auto"
              max-width="330"
              raised
            >
              <v-img
                class="align-end"
                :src="require('../assets/peak-330x180.jpg')"
              >
                <v-card-title class="card-title">三维角色动画设计</v-card-title>
              </v-img>

              <!-- <v-card-subtitle class="pb-0">Number 10</v-card-subtitle> -->

              <v-card-text class="text--primary">
                <div>
                  从原理到实际操作，介绍了建模、拓补、绑定、动画整个流程
                </div>
              </v-card-text>

              <v-card-actions>
                <div class="skill_msg">
                  <span>Lv3</span>
                  <span class="dot">.</span>
                  <span>
                    <v-icon x-small>
                      mdi-account
                    </v-icon>
                    <em>147</em>
                  </span>
                  <span class="dot">.</span>
                  <span>
                    <v-icon x-small>
                      mdi-timer
                    </v-icon>
                    <em>27</em>
                  </span>
                </div>
              </v-card-actions>
            </v-card>
          </v-row>
        </v-col>
      </v-row>

      <v-divider />

      <v-row>
        <v-col cols="12">
          <v-row class="skill_title" justify="space-between">
            <div class="skill_title--main">热门专区</div>
            <div class="more">更多>></div>
          </v-row>
          <v-row justify="center">
            <v-col cols="6">
              <div class="skill_desc">
                聚集了各行各业的人才和精英，有从业经验丰富的，也有技术过硬的，他们良心制作，倾情奉献，剖腹相授！
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-card
              v-for="n in 4"
              :key="n"
              class="ma-3 mx-auto"
              max-width="330"
              raised
            >
              <v-img
                class="align-end"
                :src="require('../assets/corselet-330x180.jpg')"
              >
                <v-card-title class="card-title"
                  >原创作品《程序猿的自我修痒》</v-card-title
                >
              </v-img>

              <!-- <v-card-subtitle class="pb-0">Number 10</v-card-subtitle> -->

              <v-card-text class="text--primary">
                <div>
                  从原理到实际操作，介绍了建模、拓补、绑定、动画整个流程
                </div>
              </v-card-text>

              <v-card-actions>
                <div class="skill_msg">
                  <span>Lv3</span>
                  <span class="dot">.</span>
                  <span>
                    <v-icon x-small>
                      mdi-account
                    </v-icon>
                    <em>147</em>
                  </span>
                  <span class="dot">.</span>
                  <span>
                    <v-icon x-small>
                      mdi-timer
                    </v-icon>
                    <em>27</em>
                  </span>
                </div>
              </v-card-actions>
            </v-card>
          </v-row>
        </v-col>
      </v-row>

      <v-divider />

      <v-row>
        <v-col cols="12">
          <v-row class="skill_title" justify="space-between">
            <div class="skill_title--main">
              <span>行业</span>
              <span class="dot">.</span>
              <span>方向</span>
            </div>
            <div class="more">更多>></div>
          </v-row>
          <v-row justify="center">
            <v-col cols="6">
              <div class="skill_desc">
                聚集了各行各业的人才和精英，有从业经验丰富的，也有技术过硬的，他们良心制作，倾情奉献，剖腹相授！
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-card
              v-for="n in 4"
              :key="n"
              class="ma-3 mx-auto"
              max-width="330"
              raised
            >
              <v-img
                class="align-end"
                :src="require('../assets/foot-330x180.jpg')"
              >
                <v-card-title class="card-title"
                  >原画《概念设计-空中之城》</v-card-title
                >
              </v-img>

              <!-- <v-card-subtitle class="pb-0">Number 10</v-card-subtitle> -->

              <v-card-text class="text--primary">
                <div>
                  从原理到实际操作，介绍了建模、拓补、绑定、动画整个流程
                </div>
              </v-card-text>

              <v-card-actions>
                <div class="skill_msg">
                  <span>Lv3</span>
                  <span class="dot">.</span>
                  <span>
                    <v-icon x-small>
                      mdi-account
                    </v-icon>
                    <em>147</em>
                  </span>
                  <span class="dot">.</span>
                  <span>
                    <v-icon x-small>
                      mdi-timer
                    </v-icon>
                    <em>27</em>
                  </span>
                </div>
              </v-card-actions>
            </v-card>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      carousels: [
        require('~/assets/highway-4800x500.jpg'),
        require('~/assets/vegetation-4800x500.jpg'),
        require('~/assets/mount-4800x500.jpg'),
        require('~/assets/tower-4800x500.jpg')
      ],
      softwares1: [
        {
          src: require('~/assets/ocean-280x100.jpg'),
          title: 'Maya',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/ocean-280x100.jpg'),
          title: '3DS MAX',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/ocean-280x100.jpg'),
          title: 'Maya',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/ocean-280x100.jpg'),
          title: '3DS MAX',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/ocean-280x100.jpg'),
          title: 'Maya',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/ocean-280x100.jpg'),
          title: 'Maya',
          artist: 'Autodesk'
        }
      ],
      softwares2: [
        {
          src: require('~/assets/light-280x100.jpg'),
          title: 'Zbrush',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/light-280x100.jpg'),
          title: 'C4D',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/light-280x100.jpg'),
          title: 'Houdinin',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/light-280x100.jpg'),
          title: 'Mari',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/light-280x100.jpg'),
          title: 'Mobox',
          artist: 'Autodesk'
        },
        {
          src: require('~/assets/light-280x100.jpg'),
          title: 'Mobox',
          artist: 'Autodesk'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
// .full-width {
//   position: absolute;
//   left: 0;
//   right: 0;
// }
.card-title {
  color: white;
}
.skill_msg {
  span {
    font-size: 12px;
    color: #999;
    /* margin-left: 18px; */
    display: inline-block;
    /* margin-top: 10px; */
    &.dot {
      margin: -6px 4px 0;
      vertical-align: middle;
    }
  }
}
.skill_title--main {
  color: orangered;
  // color: white;
  font-size: 30px;
}
.skill_title {
  font-size: 20px;
  // color: #333333;
  color: orangered;

  .more {
    font-size: 18px;
  }
  span {
    display: inline-block;
    &.dot {
      margin: -10px 4px 0;
      vertical-align: middle;
    }
  }
}
.skill_desc {
  font-size: 24px;
  color: #4c4c4c;
  text-align: center;
}
.software {
  width: 20px;
  margin: 0 auto;
  line-height: 24px;
  font-size: 20px;
  color: orangered;
}
.card-software {
  background-color: #eee;
  .v-card-subtitle {
    padding: 0 16px;
  }
}
</style>
