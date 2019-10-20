<template>
  <div>
    <div class="px-10">
      <Category />
    </div>

    <v-container>
      <v-row>
        <v-col cols="10">
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
                :src="require('../assets/fence-330x180.jpg')"
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

            <v-card
              v-for="n in 4"
              :key="n"
              class="ma-3 mx-auto"
              max-width="330"
              raised
            >
              <v-img
                class="align-end"
                :src="require('../assets/bridge-330x180.jpg')"
              >
                <v-card-title class="card-title">影视特效</v-card-title>
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
        <v-col cols="2" class="side">
          <v-card>
            <v-card-title class="side-title">
              <v-icon color="white">mdi-star</v-icon>
              猜你喜欢
              <!-- <v-img lazy-src="https://picsum.photos/330/179?random"></v-img> -->
            </v-card-title>
            <v-img :src="require('../assets/stree-330x180.jpg')"></v-img>
            <v-card-text>
              <v-list three-line>
                <v-list-item-group multiple active-class="pink--text">
                  <template v-for="index in 4">
                    <v-list-item :key="index">
                      <template v-slot:default="{ active, toggle }">
                        <v-list-item-content>
                          <v-list-item-title></v-list-item-title>
                          <v-list-item-subtitle class="text--primary">
                            通过MARI教学，掌握电影级贴图和渲染
                          </v-list-item-subtitle>
                          <v-list-item-subtitle
                            >拿好门票，进入现场!</v-list-item-subtitle
                          >
                        </v-list-item-content>

                        <v-list-item-action>
                          <v-list-item-action-text>
                            <span>
                              <v-icon x-small>
                                mdi-timer
                              </v-icon>
                              <em>27</em>
                            </span>
                            <br />
                            <span>
                              <v-icon x-small>
                                mdi-account
                              </v-icon>
                              <em>147</em>
                            </span>
                          </v-list-item-action-text>
                        </v-list-item-action>
                      </template>
                    </v-list-item>

                    <v-divider v-if="index + 1 < 5" :key="index"></v-divider>
                  </template>
                </v-list-item-group>
              </v-list>
            </v-card-text>
          </v-card>
          <v-spacer class="pa-2" />
          <v-card>
            <v-card-title class="side-title">
              <v-icon color="white">mdi-history</v-icon>
              最近浏览
              <!-- <v-img lazy-src="https://picsum.photos/330/179?random"></v-img> -->
            </v-card-title>
            <v-img :src="require('../assets/mount-330x180.jpg')"></v-img>
            <v-card-text>
              <v-list three-line>
                <v-list-item-group multiple active-class="pink--text">
                  <template v-for="index in 4">
                    <v-list-item :key="index">
                      <template v-slot:default="{ active, toggle }">
                        <v-list-item-content>
                          <v-list-item-title></v-list-item-title>
                          <v-list-item-subtitle class="text--primary">
                            通过MARI教学，掌握电影级贴图和渲染
                          </v-list-item-subtitle>
                          <v-list-item-subtitle
                            >拿好门票，进入现场!</v-list-item-subtitle
                          >
                        </v-list-item-content>

                        <v-list-item-action>
                          <v-list-item-action-text>
                            <span>
                              <v-icon x-small>
                                mdi-timer
                              </v-icon>
                              <em>27</em>
                            </span>
                            <br />
                            <span>
                              <v-icon x-small>
                                mdi-account
                              </v-icon>
                              <em>147</em>
                            </span>
                          </v-list-item-action-text>
                        </v-list-item-action>
                      </template>
                    </v-list-item>

                    <v-divider v-if="index + 1 < 5" :key="index"></v-divider>
                  </template>
                </v-list-item-group>
              </v-list>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Category from '@/components/Category'
export default {
  components: {
    Category
  },
  key: (to) => to.fullPath,
  scrollToTop: true,
  watchQuery: [
    'query',
    'page',
    'order-type',
    'order',
    'price-from',
    'price-to',
    'per_page'
  ],
  transition(to, from) {
    if (from && from.name !== 'search') {
      // console.log(this)
      // location.reload()
    }
  },
  data() {
    // <----------------------- B
    // const { routeData } = this.$store.state
    // return {
    //   meta: routeData.meta,
    //   products: routeData.items
    // }
  },
  watch: {
    $route: {
      immediate: true,
      handler(to, from) {
        // console.log(to)
        // console.log(from)
        // if (!this.$store.state.auth.account) {
        // return this.$router.push('/');
        // }
      }
    }
  },
  async asyncData({ app, route, store, error }) {
    // let post = {}
    // route.params.id = route.params.id || 1
    // if (route.params.id) {
    //   const p = await app.$axios.$get(
    //     `${process.env.apiUrl}/posts/${route.params.id}`
    //   )
    //   post = { post: p }
    // }
    // return post
  },
  // https://github.com/nuxt/nuxt.js/issues/2737
  fetch({ app, store, route }) {
    // console.log('fetch')
    // console.log(route)
    // console.log(app.router.push({ path: route.fullPath }))
    // return app.$axios
    //   .get(route.fullPath, {
    //     params: {
    //       with: ['meta', 'breadcrumbs', 'actions']
    //     }
    //   })
    //   .then((response) => {
    //     store.commit('routeDataSaved', response.data)
    //   })
  },
  mounted() {}
}
</script>

<style lang="scss" scoped>
.side-title {
  color: white;
  background: #ff9800;
}
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
</style>
