<template>
  <v-container fluid class="bg3">
    <v-layout>
      <v-flex class="text-center">
        <v-row wrap justify="center">
          <v-col cols="12" md="6">
            <v-card flat class="ma-5" outlined>
              <div class="cyan--text title mt-5" style="text-align:center">{{title[0]}}</div>
              <v-card-text style="text-align:left">
                {{caption[0]}}
                <br />
                {{caption[1]}}
              </v-card-text>
            </v-card>
            <v-card tile class="mb-5">
              <v-img width="100%" :src="src.one" />
            </v-card>

            <v-row wrap justify="left" align="center">
              <v-col cols="6" md="6 ">
                <v-card tile class="mb-5 mt-5">
                  <v-img width="100%" :src="src.two" />
                </v-card>
              </v-col>
              <v-col cols="6" md="6">
                <v-card flat outlined class="mb-5 mt-5">
                  <v-card-text style="text-align:left">
                    {{caption[2]}}
                    <br />
                    {{caption[3]}}
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>

            <v-row wrap justify="left" align="center">
              <v-col cols="6" md="6">
                <v-card flat outlined class="mb-5 mt-5">
                  <v-card-text style="text-align:left">
                    {{caption[4]}}
                    <br />
                    {{caption[5]}}
                  </v-card-text>
                </v-card>
              </v-col>
              <v-col cols="6" md="6">
                <v-card tile class="mb-5 mt-5">
                  <v-img width="100%" :src="src.three" />
                </v-card>
              </v-col>
            </v-row>

            <v-card flat class="ma-5" outlined>
              <div class="cyan--text title mt-5" style="text-align:center">{{title[1]}}</div>
              <v-card-text style="text-align:left;">{{caption[6]}}</v-card-text>
            </v-card>
            <v-card tile class="mb-5">
              <v-img width="100%" :src="src.four" />
            </v-card>
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
      src: {
        one: require("~/assets/work/脳トレ/キャプション1.png"),
        two: require("~/assets/work/脳トレ/キャプション6.png"),
        three: require("~/assets/work/脳トレ/キャプション3.png"),
        four: require("~/assets/work/脳トレ/キャプション4.png")
      },
      caption: [
        "　子供やお年寄りを対象とした癒し系脳トレアプリをコンセプトにした本作品は、動物たちが織り成すシンプルなUIかつ夢中になれるゲーム内容に重きを置いて制作されました。",
        "　スタンダードなじゃんけん、タイムアタックパズル、短期記憶鍛錬など、6つのゲームがあり、それぞれを「かんたん」から「むずかしい」までの3つの難易度でプレイすることができます。",
        "　本ゲームには、きりん、ライオン、羊、猫など馴染み深い動物たちが多数登場し、脳トレを楽しませてくれます。",
        "　私は主にタイトルロゴ、動物のイラスト、UIデザイン、ゲームプログラミングを担当させていただきました。",
        "　やりこみ要素としてメダルコンプリートがあり、クリアタイムや合計解答数などによって貰えるメダルが変化します。",
        "　また、メダルを全部集めることにより動物たちから特別なコメントを貰うことができます。",
        "　こちらの写真は実際に群馬県内の病院で認知機能のリハビリに使用していただいた時の様子です。(患者様の掲載許可を得ています。)ブラウザでも表示できるお手軽さと大きなボタンでの操作で患者様から非常に高評価をいただくことができました。"
      ],
      title: ["『脳トレ＆アニマルズ』", "『リハビリへの応用』", ""]
    };
  }
};
</script>

<style lang="scss" scoped>
.bg-n {
  background-color: #fefcf1;
  color: #fefcf1;
}
</style>