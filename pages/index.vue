<template>
  <v-layout class="bg">
    <v-flex class="text-center mt-5">
      <v-row wrap justify="center">
        <v-col cols="12" sm="6">
          <v-card flat height="400px">
            <v-list-item>
              <v-list-item-content>
                <!-- <div class="overline mb-4">OVERLINE</div> -->
                <v-avatar size="150" class="mt-5">
                  <img src="~/assets/me.jpg" alt="me" />
                </v-avatar>
                <v-list-item-title class="headline mt-5">
                  <div class="m-custom mr-5">
                    <v-icon left class="mb-1" color="c2">mdi-account</v-icon>ABOUT ME
                  </div>
                </v-list-item-title>

                <!-- <v-list-item-subtitle> <aboutme /> </v-list-item-subtitle> -->
              </v-list-item-content>
            </v-list-item>
            <v-card-text>
              <aboutme />
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-flex>
  </v-layout>
</template>

<style lang="scss" scoped></style>

<script>
import Aboutme from "~/components/aboutme";

export default {
  components: {
    Aboutme
  },
  data() {
    return {};
  }
};
</script>
