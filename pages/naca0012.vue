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
                <v-card tile class="mb-5 mt-5 pa-5">
                  <v-img width="100%" :src="src.two" />
                </v-card>
              </v-col>
              <v-col cols="6" md="6">
                <v-card flat outlined class="mb-5 mt-5">
                  <v-card-text style="text-align:left">
                    {{caption[2]}}
                    <!-- <br />
                    {{caption[3]}}-->
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>

            <v-row wrap justify="left" align="center">
              <v-col cols="6" md="6">
                <v-card flat outlined class="mb-5 mt-5">
                  <v-card-text style="text-align:left">{{caption[3]}}</v-card-text>
                </v-card>
              </v-col>
              <v-col cols="6" md="6">
                <v-card tile class="mb-5 mt-5">
                  <v-img width="100%" :src="src.three" />
                </v-card>
                <v-card tile class="mb-5 mt-5">
                  <v-img width="100%" :src="src.four" />
                </v-card>
              </v-col>
            </v-row>

            <!-- <v-card flat class="ma-5" outlined>
              <div class="cyan--text title mt-5" style="text-align:center">{{title[1]}}</div>
              <v-card-text style="text-align:left;">{{caption[6]}}</v-card-text>
            </v-card>
            <v-card tile class="mb-5">
              <v-img width="100%" :src="src.four" />
            </v-card>-->
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
        one: require("~/assets/work/大学/キャプション1.jpg"),
        two: require("~/assets/work/大学/キャプション2.jpg"),
        three: require("~/assets/work/大学/キャプション3.jpg"),
        four: require("~/assets/work/大学/キャプション4.jpg")
      },
      caption: [
        "　大学では応用流体工学研究室で数値シミュレーションを専攻していました。計算格子を用いてシミュレーションが行えるようにFortranでアルゴリズムを記述し、FLScopeで実際の流れを可視化することに成功しました。",
        "　過去に例がない計算法でのシミュレーションであったため、流体工学の先生方からは非常に高い評価を得ました。",
        "　左図は本計算のアルゴリズム図です。細かい概要は省きますが、あらかじめ図としてアウトプットしてから計画的にコーディングを行ったことは、他の言語を効率的に記述する場合にも非常に役立っています。",
        "　研究の目標といたしまして、代入数値を様々に変えることができることを目指して計算アルゴリズムを改良していきました。右図は温度分布図ですが、流体の不規則な動きも正確に捉える事ができます。",
        "　やりこみ要素としてメダルコンプリートがあり、クリアタイムや合計解答数などによって貰えるメダルが変化します。",
        "　また、メダルを全部集めることにより動物たちから特別なコメントを貰うことができます。",
        "　こちらの写真は実際に群馬県富岡市の病院で認知機能のリハビリに使用していただいた時の様子です。ブラウザでも表示できるお手軽さと大きなボタンでの操作で患者様から非常に高評価をいただくことができました。"
      ],
      title: ["『翼周りの数値シミュレーション』", "『リハビリへの応用』", ""]
    };
  }
};
</script>

<style>
</style>