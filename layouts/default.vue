<template>
  <div>
    <v-app id="inspire">
      <v-navigation-drawer
        v-model="drawer"
        :clipped="clipped"
        fixed
        app
        disable-resize-watcher
      >
        <v-list>
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :to="item.to"
            router
            exact
          >
            <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title v-text="item.title" />
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-app-bar :clipped-left="clipped" fixed app color="c4">
        <v-app-bar-nav-icon
          @click.stop="drawer = !drawer"
          class="hidden-md-and-up"
        />
        <v-toolbar-title v-text="title" class="custom" to="/" />
        <!-- <sizebtn /> -->
        <v-spacer />

        <v-toolbar-items
          v-for="(item, i) in items"
          :key="i"
          class="hidden-sm-and-down"
        >
          <v-btn :to="item.to" text color="c1">
            <v-icon left>{{ item.icon }}</v-icon>
            <div style="font-family:'cp';">{{ item.title }}</div>
          </v-btn>
        </v-toolbar-items>
      </v-app-bar>

      <v-content>
        <nuxt />
      </v-content>

      <v-footer color="c1">
        <v-col class="text-center" cols="12">
          <span class="ft">&copy;2020 Hidesato Nakamura</span>
        </v-col>
      </v-footer>
    </v-app>
  </div>
</template>

<style lang="scss">
.custom {
  font-family: "cp";
  font-size: 40px;
  color: #2b4f58;
}
.m-custom {
  font-family: "cp";
  color: #2b4f58;
}
.ft {
  font-size: 10px;
  color: white;
}
.bg {
  background-image: url("~@/assets/p2.jpg");
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background-size: 110%;
  background-color: rgba(255, 255, 255, 0.5);
  background-blend-mode: lighten;
}
.bg2 {
  background-image: url("~@/assets/p4.jpg");
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background-size: 100%;
  background-color: rgba(255, 255, 255, 0.6);
  background-blend-mode: lighten;
}
#inspire {
  background: none;
}
</style>

<script>
import Sizebtn from "~/components/size";

export default {
  components: {
    Sizebtn
  },
  data() {
    return {
      clipped: true,
      drawer: false,
      items: [
        {
          icon: "mdi-account",
          title: "Profile",
          to: "/"
        },
        {
          icon: "mdi-cursor-pointer",
          title: "Skill",
          to: "/skill"
        },
        {
          icon: "mdi-folder-multiple-outline",
          title: "Works",
          to: "/works"
        },
        {
          icon: "mdi-email",
          title: "Contact",
          to: "/contact"
        }
      ],
      right: true,
      rightDrawer: false,
      title: "Portfolio",
      fixed: true
    };
  }
};
</script>
