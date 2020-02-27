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
            <!-- <v-card tile class="mb-5">
              <v-img width="100%" :src="src.one" />
            </v-card>-->

            <v-row wrap justify="left" align="center">
              <v-col cols="6" md="6 ">
                <v-card tile class="mb-5 mt-5">
                  <v-img width="100%" :src="src.one" />
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
        one: require("~/assets/work/口腔ケア/キャプション1.png"),
        two: require("~/assets/work/脳トレ/キャプション6.png"),
        three: require("~/assets/work/脳トレ/キャプション3.png"),
        four: require("~/assets/work/脳トレ/キャプション4.png")
      },
      caption: [
        "　高齢者の方は飲み込む力の低下により気管に食べ物が誤って入り、重大な症状を引き起こす場合があります。",
        "　病院で高齢者向けに誤嚥防止ガイダンスが開かれる際、こちらに使われている女性のイラストをボランティアで作成させていただきました。(イラスト以外は別の方の編集です。)",
        "　高齢者でも見やすいように大きな文字で見やすくデザインしてくださっています。",
        "　ガイダンスは約1時間程で、説明の後に資料に従って来場者一同での実演が行われました。"
      ],
      title: ["『高齢者向けお口の体操』"]
    };
  }
};
</script>

<style>
</style>