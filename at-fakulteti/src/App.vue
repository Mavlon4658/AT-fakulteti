<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <v-sheet
        color="grey lighten-4"
        class="pa-4"
      >
        <v-avatar
          class="mb-4"
          color="grey darken-1"
          size="64"
        ></v-avatar>

        <div>john@vuetifyjs.com</div>
      </v-sheet>
      <v-card
        class="mx-auto"
        max-width="500"
      >
        <v-list>
          <v-list-item-group v-model="model">
            <v-list-item
              v-for="(item, i) in items"
              :key="i"
              router
              :to="item.to"
            >
              <v-list-item-icon>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title>{{item.text}}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-card>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({ 
    drawer: null,
    items: [
        {
          icon: 'mdi-home',
          text: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-book',
          text: 'About',
          to: '/about'
        },
        {
          icon: 'mdi-account-school',
          text: 'Students',
          to: '/students'
        },
        {
          icon: 'mdi-phone',
          text: 'Contact',
          to: '/contact'
        },
        {
          icon: 'mdi-newspaper-variant-outline',
          text: 'More',
          to: '/more'
        },
      ],
      model: 1,
    }),
};
</script>
