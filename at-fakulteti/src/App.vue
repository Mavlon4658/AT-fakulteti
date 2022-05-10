<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app class="bg-color">
      <v-sheet
        color="cyan lighten-5"
        class="pa-4 bg-color"
        align="center"
        justify="center"
      >
        <v-avatar
          class="mb-4 bg-color"
          color="cyan lighten-2"
          size="100"
          justify-center
        >
          <img src="images/AT-logo.jpg" alt="" />
        </v-avatar>

        <div>
          <b>Axborot Texnologiyalari fakulteti</b>
        </div>
      </v-sheet>
      <v-card class="mx-auto" max-width="500" color="cyan lighten-5">
        <v-list>
          <v-list-item-group v-model="model">
            <v-list-item
              hover
              v-for="(item, i) in items"
              :key="i"
              router
              :to="item.to"
            >
              <v-list-item-icon>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>{{ item.text }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-card>
    </v-navigation-drawer>

    <v-app-bar app class="bg-dark">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title class="text"
        >AMALIY MATEMATIKA VA INFORMATIKA</v-toolbar-title
      >
    </v-app-bar>

    <v-main class="main_bg">
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: null,
    items: [
      {
        icon: "mdi-home",
        text: "Home",
        to: "/",
      },
      {
        icon: "mdi-book",
        text: "About",
        to: "/about",
      },
      {
        icon: "mdi-account-school",
        text: "Students",
        to: "/students",
      },
      {
        icon: "mdi-phone",
        text: "Contact",
        to: "/contact",
      },
      {
        icon: "mdi-newspaper-variant-outline",
        text: "More",
        to: "/more",
      },
    ],
    model: 1,
  }),
};
</script>

<style scoped>
img {
  object-fit: cover;
  transform: scale(1.3);
}

.text {
  color: rgb(39, 37, 37) !important;
}

.bg-dark {
  background-color: #bbdefb !important;
}

.main_bg {
  background-color: #e3f2fd !important;
}
.bg-color {
  color: #e0f7fa !important;
}
</style>
