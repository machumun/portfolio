<template>
  <v-card class="mx-auto" color="c4" height="200px">
    <!-- <img width="100%" src="../assets/p2.jpg" /> -->
    <v-card-title class="cardtitle">
      {{ item.title }}
      <!-- <v-spacer></v-spacer>
      使用歴 {{ item.career }} 年 -->
    </v-card-title>
    <v-rating
      :value="item.rating"
      background-color="c3"
      color="c5"
      dense
      half-increments
      readonly
      size="20"
    />
    <v-card-subtitle style="text-align:left;">
      {{ item.comment }}
    </v-card-subtitle>
  </v-card>
</template>

<style lang="scss" scoped>
.cardtitle {
  font-size: 16px;
  color: #2b4f58;
  margin: 5px;
  padding: 5px;
}
.career {
  text-align: right;
}
</style>

<script>
export default {
  props: {
    item: { title: String, comment: String, rating: Number, career: Number }
  }
};
</script>
