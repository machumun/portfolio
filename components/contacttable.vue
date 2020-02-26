<template>
  <v-simple-table>
    <template v-slot:default>
      <!-- <thead>
        <tr>
          <th class="text-left">Name</th>
          <th class="text-left">Calories</th>
        </tr>
      </thead> -->
      <tbody>
        <tr v-for="item in desserts" :key="item.name">
          <td style="text-align:left;">
            <v-icon left>{{ item.icon }}</v-icon
            >{{ item.name }}
          </td>
          <v-spacer />
          <td v-if="!item.link">{{ item.detail }}</td>
          <td v-if="item.link">
            <a :href="item.path">{{ item.detail }}</a>
          </td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</template>
<style lang="scss" scoped>
td {
  color: #2b4f58;
}
</style>

<script>
export default {
  data() {
    return {
      desserts: [
        {
          name: "E-Mail",
          detail: "hidesto.nakamura1@gmail.com",
          icon: "mdi-mail",
          link: false,
          path: ""
        },
        {
          name: "住所",
          detail: "滋賀県大津市",
          icon: "mdi-map-marker",
          link: false,
          path: ""
        },
        {
          name: "Github",
          detail: "Hina0710",
          icon: "mdi-github-circle",
          link: true,
          path: "https://github.com/Hina0710"
        }
      ]
    };
  }
};
</script>
