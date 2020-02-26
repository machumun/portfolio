<template>
  <v-container>
    <v-layout>
      <v-flex class="text-center">
        <v-row wrap justify="center">
          <v-col cols="6">
            <v-list-item-title class="headline mt-5">
              <div class="m-custom">
                <v-icon left class="mb-1" color="c2"
                  >mdi-folder-multiple-outline</v-icon
                >WORKS
              </div>
            </v-list-item-title>
          </v-col>
        </v-row>
        <v-row wrap justify="center">
          <v-col cols="12" sm="6">
            <v-row justify="left">
              <v-col
                v-for="(item, i) in works"
                :key="i"
                cols="12"
                lg="4"
                md="6"
              >
                <workcard :item="item" /> </v-col
            ></v-row>
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
          to: "/",
          title: "脳トレ＆アニマルズ"
        },
        {
          path: require("~/assets/work/お口の体操2.jpg"),
          to: "/",
          title: "富岡市七日市病院リハ"
        },
        {
          path: require("~/assets/work/person.jpg"),
          to: "/",
          title: "イラスト"
        },
        {
          path: require("~/assets/work/機械工学発表.jpg"),
          to: "/",
          title: "流体シミュレーション"
        }
      ]
    };
  }
};
</script>
