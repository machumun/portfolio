<template>
  <v-container>
    <v-layout>
      <v-flex class="text-center">
        <v-row wrap justify="center">
          <v-col cols="6">
            <v-list-item-title class="headline mt-5">
              <div class="m-custom">
                <v-icon left class="mb-1" color="c2">mdi-cursor-pointer</v-icon
                >SKILL
              </div>
            </v-list-item-title>
          </v-col>
        </v-row>

        <v-card flat>
          <v-card-title>
            <v-icon left color="c2">mdi-monitor</v-icon>
            Web系
          </v-card-title>
        </v-card>
        <v-row wrap justify="center">
          <v-col v-for="(item, i) in webitems" :key="i" cols="12" md="3" sm="4">
            <skillcard :item="item" />
          </v-col>
        </v-row>

        <v-card flat>
          <v-card-title>
            <v-icon left color="c2">mdi-database</v-icon>
            DB
          </v-card-title>
        </v-card>
        <v-row wrap justify="center">
          <v-col v-for="(item, i) in db" :key="i" cols="12" md="3" sm="4">
            <skillcard :item="item" />
          </v-col>
        </v-row>

        <v-card flat>
          <v-card-title>
            <v-icon left color="c2">mdi-calculator</v-icon>
            制御・業務系
          </v-card-title>
        </v-card>

        <v-row wrap justify="center">
          <v-col
            v-for="(item, i) in workitems"
            :key="i"
            cols="12"
            md="3"
            sm="4"
          >
            <skillcard :item="item" />
          </v-col>
        </v-row>

        <v-card flat>
          <v-card-title>
            <v-icon left color="c2">mdi-pencil</v-icon>
            画像編集ソフト
          </v-card-title>
        </v-card>

        <v-row wrap justify="center">
          <v-col v-for="(item, i) in softs" :key="i" cols="12" md="3" sm="4">
            <skillcard :item="item" />
          </v-col>
        </v-row>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<style lang="scss"></style>

<script>
import Skillcard from "~/components/skillcard";

export default {
  components: {
    Skillcard
  },
  data() {
    return {
      webitems: [
        {
          title: "JavaScript",
          rating: 4,
          comment:
            "フロントとバックに一貫して使用。友人と開発した脳トレアプリゲームをGooglePlayStoreでリリースした経験あり。",
          career: 1
        },
        {
          title: "HTML5",
          rating: 3,
          comment: "主にJavaScriptとの併用で使用。基本的な事はできます。",
          career: 1
        },
        {
          title: "CSS/SCSS",
          rating: 2.5,
          comment: "本サイトのcssフレームワークにはVuetifyを使用しています。",
          career: 1
        }
      ],
      workitems: [
        {
          title: "C言語",
          rating: 4.5,
          comment: "ほとんどの機能を習得しています。",
          career: 1
        },
        {
          title: "C++",
          rating: 3,
          comment: "グラフィックの行列計算程度は扱うことができます。",
          career: 1
        },
        {
          title: "Fortran",
          rating: 5,
          comment:
            "複雑な計算式を扱う事ができ、実務レベルでのシミュレーションが可能です。",
          career: 1
        }
      ],
      softs: [
        {
          title: "CLIP STUDIO PAINT",
          rating: 5,
          comment:
            "イラスト制作から色彩校正、製本まで、必要な機能を一通り扱えます。",
          career: 1
        },
        {
          title: "Adobe Photoshop",
          rating: 3,
          comment: "スプライトシート編集での使用経験あり。",
          career: 1
        }
      ],
      db: [
        {
          title: "Firebase",
          rating: 3,
          comment:
            "身内向けにTETRIS風のパズルゲームを公開。その時のスコアランキングの処理に使用。",
          career: 1
        },
        {
          title: "MySQL",
          rating: 3,
          comment:
            "現在開発中のWebアプリケーションでのアカウント情報管理に使用。",
          career: 1
        },
        {
          title: "MongoDB",
          rating: 2.5,
          comment: "",
          career: 1
        }
      ]
    };
  }
};
</script>
