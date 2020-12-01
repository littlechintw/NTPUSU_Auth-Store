<template>
  <v-app>
    <!-- <v-card class="overflow-hidden"> -->
    <v-app-bar app dark inverted-scroll="invertedScroll">
      <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

      <v-toolbar-title>臺北大學特約店家</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn
        rounded
        href="https://www.google.com/maps/d/edit?mid=1FG6nbX7nVaz5NvasFz-2s6CgZ5dUHHbE"
        target="_blank"
      >
        Google Map
        <v-icon right dark>mdi-map</v-icon>
      </v-btn>
    </v-app-bar>
    <v-content>
      <v-card>
        <v-content>
          <router-view />
        </v-content>

        <v-footer padless class="font-weight-medium">
          <v-col class="text-center" cols="12" style="font-size: 14px">
            &copy; {{ new Date().getFullYear() }} Copyright
            <a href="https://littlechintw.github.io">littlechintw.github.io</a>.
            All rights reserved.
          </v-col>
        </v-footer>
      </v-card>
    </v-content>

    <!-- <v-app-bar
      absolute
      color="primary"
      dark
      inverted-scroll
      scroll-target="#scrolling-techniques-8"
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>臺北大學特約店家</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    <v-sheet
      id="scrolling-techniques-8"
      class="overflow-y-auto"
      max-height="95%"
    >
      <v-content>
        <v-container fluid>
          <v-row>
            <v-col cols="12">
              <v-row align="center" justify="center">
                <router-view />
              </v-row>
            </v-col>
          </v-row>
        </v-container>
      </v-content>

      <v-footer padless class="font-weight-medium">
        <v-col class="text-center" cols="12" style="font-size: 14px">
          &copy; {{ new Date().getFullYear() }} Copyright
          <a href="https://littlechintw.github.io">littlechintw.github.io</a>.
          All rights reserved.
        </v-col>
      </v-footer>
    </v-sheet> -->

    <!-- </v-card> -->
    <!-- <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <h1>臺北大學特約店家</h1>
      </div>

      <v-spacer></v-spacer>

      <v-btn href="/" icon>
        <v-icon>home</v-icon>
      </v-btn>

      <v-btn href="about" icon>
        <v-icon>help_outline</v-icon>
      </v-btn>
    </v-app-bar> -->
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({}),
};
</script>
