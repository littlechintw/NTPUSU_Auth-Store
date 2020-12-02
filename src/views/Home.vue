<template>
  <div class="home">
    <!-- 標題區塊 -->
    <v-parallax
      dark
      src="https://i.ibb.co/ynVm9kF/PXL-20200928-133003286-NIGHT.jpg"
      :height="window_height * 0.6"
    >
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <h1 style="font-size: 4.8rem">臺北大學特約店家</h1>
          <h4 style="font-size: 2rem">
            北大周圍大大小小的店家，到底有哪些有學生優惠勒？！
          </h4>
          <h4 style="font-size: 2rem">快來看看吧❤️</h4>
        </v-col>
      </v-row>
    </v-parallax>

    <!-- 出示學生證區塊 -->
    <v-card
      class="d-flex align-content-center justify-center flex-wrap"
      :height="window_height * 0.3"
      color="#619D6A"
      flat
      tile
      min-height="200"
      align="center"
    >
      <v-card class="align-self-center" color="#619D6A" flat>
        <v-img
          src="https://i.ibb.co/n1f8cRs/stu-card.png"
          :height="window_height * 0.3 * 0.75"
          :max-width="((window_height * 0.3 * 0.75) / 54) * 90"
        />
      </v-card>

      <v-card
        class="align-self-center"
        color="#619D6A"
        flat
        :min-width="window_width * 0.25"
      >
        <h4 style="font-size: 1.8rem">出示學生證，享有優惠</h4>
      </v-card>
    </v-card>

    <!-- 商家區塊 -->
    <v-card class="align-self-center" color="#CFD386" flat>
      <br />
      <v-container class="pa-1">
        <v-item-group
          v-model="selected"
          multiple
          v-for="category in list_data"
          :key="category"
        >
          <h1>{{ category.title }}</h1>
          <v-divider /><br />

          <v-container>
            <v-row justify="center">
              <v-col v-for="store in category.store" :key="store" cols="auto">
                <v-card elevation="6" width="374">
                  <template slot="progress">
                    <v-progress-linear
                      color="deep-purple"
                      height="10"
                      indeterminate
                    ></v-progress-linear>
                  </template>

                  <v-img
                    height="250"
                    :src="`data:image/png;base64,${store.img}`"
                    v-if="data_detect(store.img)"
                  ></v-img>

                  <v-card-title style="font-size: 30px">
                    {{ store.title }}
                  </v-card-title>

                  <v-divider />

                  <v-card-text>
                    <div style="font-size: 20px">
                      <b>{{ store.subtitle }}</b>
                    </div>
                  </v-card-text>

                  <v-card-text>
                    <div style="font-size: 18px">
                      {{ store.discount }}
                    </div>
                  </v-card-text>

                  <v-card-actions>
                    <v-btn
                      color="deep-purple lighten-2"
                      outlined
                      :href="store.website"
                      target="_blank"
                      v-if="data_detect(store.website)"
                    >
                      網頁
                    </v-btn>
                    <v-btn
                      color="deep-purple lighten-2"
                      outlined
                      :href="map_url(store.map, store.title)"
                      target="_blank"
                    >
                      地圖搜尋
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-item-group>
      </v-container>
      <br />
      <v-card color="#CFD386" flat tile align="center">
        <h1 style="font-size: 2.8rem">更多特約店家持續更新中！</h1>
      </v-card>
      <br />
    </v-card>

    <!-- 聯絡區塊 -->
    <v-card color="#86C0D3" flat tile align="center">
      <br />
      <h1 style="font-size: 4.8rem">聯絡我們</h1>
    </v-card>
    <v-card
      class="d-flex align-content-center justify-space-around flex-wrap"
      :height="window_height * 0.2"
      color="#86C0D3"
      flat
      tile
      align="center"
    >
      <v-card class="align-self-center" color="#86C0D3" flat>
        <v-btn rounded x-large href="https://www.facebook.com/NTPUSU">
          <v-icon left dark>mdi-facebook</v-icon>
          Facebook
        </v-btn>
      </v-card>

      <v-card class="align-self-center" color="#86C0D3" flat>
        <v-btn rounded x-large href="https://www.instagram.com/ntpu_su">
          <v-icon left dark>mdi-instagram</v-icon>
          Instagram
        </v-btn>
      </v-card>
    </v-card>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld,
  },
  data: () => ({
    window_height: 700,
    window_width: 1600,
    list_data: [],
  }),
  methods: {
    data_detect(input) {
      if (input == "") return false;
      else return true;
    },
    map_url(input, place) {
      if (input == "") return "https://www.google.com.tw/maps/search/" + place;
      else return input;
    },
  },
  created: function () {
    console.log("Init");
    console.log(window.innerHeight);
    this.window_height = window.innerHeight;
    this.window_width = window.innerWidth;
    this.list_data = this.GLOBAL.full_store_list;
    console.log(this.list_data);
  },
};
</script>
