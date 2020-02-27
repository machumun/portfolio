<template>
  <v-container fluid class="bg3">
    <v-layout>
      <v-flex class="text-center">
        <v-row wrap justify="center">
          <v-col cols="12" md="6">
            <v-card flat class="d-inline-block mx-auto mt-5">
              <v-container>
                <v-row justify="space-between">
                  <v-col cols="auto" class="hidden-md-and-down">
                    <img height="200" :src="src[0]" />
                  </v-col>

                  <v-col cols="auto" class="text-center pl-0">
                    <v-row class="flex-column ma-0 fill-height" justify="center">
                      <v-card-text style="text-align:left">
                        在学時、1年次から卒業時まで大変注力した物事ですが
                        <br />版権物や掲載NGのご依頼もの、成人向けなどが多い為
                        <br />本ポートフォリオでは一部のみ掲載しています。
                      </v-card-text>
                    </v-row>
                  </v-col>
                </v-row>
              </v-container>
            </v-card>

            <v-card class="ma-5" @click="overlay=!overlay;i=1;">
              <v-img :src="src[1]" />
            </v-card>

            <v-card class="ma-5" @click="overlay=!overlay;i=2;">
              <v-img :src="src[2]" />
            </v-card>

            <!-- <v-card class="ma-5" @click="overlay=!overlay;i=3;" >
              <v-img :src="src[3]" />
            </v-card>-->

            <v-overlay :value="overlay">
              <v-card width="400px" class="ma-5">
                <v-img :src="src[i]">
                  <v-row justify="end">
                    <v-col cols="3">
                      <v-btn @click="overlay = false" color="black" icon small>
                        <v-icon>mdi-close</v-icon>
                      </v-btn>
                    </v-col>
                  </v-row>
                </v-img>
              </v-card>
            </v-overlay>
          </v-col>
        </v-row>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      src: [
        require("~/assets/work/工事中.png"),
        require("~/assets/work/イラスト/キャプション.jpg"),
        require("~/assets/work/イラスト/キャプション4.jpg"),
        require("~/assets/work/イラスト/キャプション3.jpg")
      ],
      overlay: false,
      i: 0
    };
  }
};
</script>

<style>
</style>