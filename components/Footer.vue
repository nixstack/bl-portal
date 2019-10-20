<template>
  <v-footer dark class="fixed-bottom">
    <div class="tt"></div>
    <v-container class="content">
      <v-row>
        <v-col>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>关于我们</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-subtitle>加入我们</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-subtitle>网站地图</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>发现更多</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-subtitle>寻求合作</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-subtitle>意见反馈</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>联系我们</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-subtitle>商业洽谈</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>关注我们</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-col>
        <v-col>
          <v-list-item>
            <v-list-item-content>
              <!-- <div class="tt"></div> -->
              <div>
                <v-img :src="require('../assets/qcode.png')" width="100" />
              </div>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>关注服务号，不定时推送</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<style lang="scss" scoped>
// .tt {
//   background: url('~assets/57-330x180.jpg');
//   height: 100px;
// }
.fixed-bottom {
  position: relative;
  bottom: 0;
  left: 0;
  right: 0;
  .container {
    padding: 0;
    .col {
      padding-top: 0;
      padding-bottom: 0;
    }
  }
  .v-list-item {
    min-height: 20px;
  }
}
</style>
