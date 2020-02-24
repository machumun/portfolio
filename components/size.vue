<template>
  <v-card>
    <v-btn class="hidden-lg-and-down">
      xl
      <!-- このボタンはxlの時しか表示されません -->
    </v-btn>
    <v-btn class="hidden-md-and-down hidden-xl-only">
      lg
      <!-- このボタンはlgの時しか表示されません -->
    </v-btn>
    <v-btn class="hidden-lg-and-up hidden-sm-and-down">
      md
      <!-- このボタンはmdの時しか表示されません -->
    </v-btn>
    <v-btn class="hidden-md-and-up hidden-xs-only">
      sm
      <!-- このボタンはsmの時しか表示されません -->
    </v-btn>
    <v-btn class="hidden-sm-and-up">
      xs
      <!-- このボタンはxsの時しか表示されません -->
    </v-btn>
  </v-card>
</template>

<script>
export default {};
</script>
