<template>
  <v-hover v-slot:default="{ hover }">
    <v-card :to="item.to" :elevation="hover ? 6 : 2" :class="{ 'on-hover': hover }" tile>
      <v-img width="100%" height="200" :src="item.path" />
      <v-card-title class="overline">{{ item.title }}</v-card-title>
    </v-card>
  </v-hover>
</template>

<style lang="scss" scoped>
.v-card {
  transition: opacity 0.4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
}

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>

<script>
export default {
  props: { item: { path: String, to: String, title: String } }
};
</script>
