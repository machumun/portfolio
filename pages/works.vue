<template>
  <v-container fluid class="bg3">
    <v-layout>
      <v-flex class="text-center">
        <v-row wrap justify="center">
          <v-col cols="6">
            <v-list-item-title class="headline mt-5">
              <div class="m-custom">
                <v-icon left class="mb-1" color="c2">mdi-folder-multiple-outline</v-icon>WORKS
              </div>
            </v-list-item-title>
          </v-col>
        </v-row>
        <v-row wrap justify="center">
          <v-col cols="12" sm="7">
            <v-row justify="left">
              <v-col v-for="(item, i) in works" :key="i" cols="12" lg="4" md="6">
                <workcard :item="item" />
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import Workcard from "~/components/workcard";

export default {
  components: { Workcard },
  data() {
    return {
      works: [
        {
          path: require("~/assets/work/脳トレ＆アニマルズ.jpg"),
          to: "/notore",
          title: "脳トレ＆アニマルズ"
        },
        {
          path: require("~/assets/work/お口の体操2.jpg"),
          to: "/okuti",
          title: "高齢者向け資料 イラスト担当"
        },
        {
          path: require("~/assets/work/person.jpg"),
          to: "/illust",
          title: "イラスト"
        },
        {
          path: require("~/assets/work/機械工学発表.jpg"),
          to: "/naca0012",
          title: "流体シミュレーション"
        }
      ]
    };
  }
};
</script>
