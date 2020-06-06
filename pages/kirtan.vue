<template>
  <v-container class="pa-4 text-center">
    <v-row class="fill-height" align="center" justify="center">
      <template v-for="(item, i) in items">
        <v-col
          :key="i"
          cols="12"
          md="4"
        >
          <v-hover v-slot:default="{ hover }">
            <v-card
              :elevation="hover ? 12 : 2"
              :class="{ 'on-hover': hover }"
            >
              <v-img
                :src="item.img"
                height="225px"
              >
                <v-card-title class="title white--text">
                  <v-row
                    class="fill-height flex-column"
                    justify="space-between"
                  >
                    <p class="mt-4 subheading text-left">{{ item.title }}</p>

                    <div>
                      <p class="ma-0 body-1 font-weight-bold font-italic text-left">
                        {{ item.text }}
                      </p>
                      <p class="caption font-weight-medium font-italic text-left">
                        {{ item.subtext }}
                      </p>
                    </div>

                    <div class="align-self-center">
                      <v-btn
                        v-for="(icon, index) in icons"
                        :key="index"
                        :class="{ 'show-btns': hover }"
                        color="transparent"
                        icon
                      >
                        <v-icon
                          :class="{ 'show-btns': hover }"
                          color="transparent"
                        >
                          {{ icon }}
                        </v-icon>
                      </v-btn>
                    </div>
                  </v-row>
                </v-card-title>
              </v-img>
            </v-card>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      icons: ['mdi-rewind', 'mdi-play', 'mdi-fast-forward'],
      items: [
        {
          title: '24H Kirtan',
          text: "It's Every Ekadashi",
          subtext: 'Chant and be Happy',
          img: 'https://scontent.fnag1-1.fna.fbcdn.net/v/t31.0-8/12719229_1223872547640953_7851874836960444245_o.jpg?_nc_cat=102&_nc_sid=6e5ad9&_nc_ohc=SyppD0kt0i4AX9P9Ufb&_nc_ht=scontent.fnag1-1.fna&oh=744e99a34e646d5674d00e67e05979c2&oe=5F016037',
        },
        {
          title: 'Kirtan Festival',
          text: 'Greatest Kirtanias',
          subtext: 'Lose yourself in Devotion.',
          img: 'http://radhagopinath.com/new/wp-content/uploads/2018/01/IMG_32051.jpg',
        },
        {
          title: 'Kids Kirtan Mela',
          text: 'By Kids',
          subtext: 'Every month',
          img: 'http://www.iskconpune.com/dev/wp-content/uploads/2017/09/DSC_0158.jpg',
        },
      ],
      transparent: 'rgba(255, 255, 255, 0)',
    }),
  }
</script>

<style scoped>
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
 }

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>