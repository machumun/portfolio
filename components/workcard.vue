<template>
  <v-card :to="item.to" tile>
    <v-img width="100%" height="200" :src="item.path" />
    <v-card-title class="overline">{{ item.title }}</v-card-title>
  </v-card>
</template>

<style lang="scss" scoped></style>

<script>
export default {
  props: { item: { path: String, to: String, title: String } }
};
</script>
