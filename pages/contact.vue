<template>
  <v-layout class="bg2">
    <v-container>
      <v-layout>
        <v-flex class="text-center">
          <v-row wrap justify="center">
            <v-col cols="6">
              <v-list-item-title class="headline mt-5">
                <div class="m-custom">
                  <v-icon left class="mb-1" color="c2">mdi-email</v-icon>CONTACT
                </div>
              </v-list-item-title>
            </v-col>
          </v-row>
          <v-row wrap justify="center">
            <v-col cols="12" sm="4"><contact-table /> </v-col
          ></v-row>
        </v-flex>
      </v-layout>
    </v-container>
  </v-layout>
</template>

<script>
import ContactTable from "~/components/contacttable";

export default {
  components: {
    ContactTable
  }
};
</script>
