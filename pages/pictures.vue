<template>
  <v-carousel>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://media-cdn.tripadvisor.com/media/photo-s/07/19/6a/73/iskcon-nvcc-temple.jpg',
          },
          {
            src: 'http://centers.iskcondesiretree.com/wp-content/uploads/2013/02/Jagannth-Baladeva-Subhadra.jpg',
          },
          {
            src: 'http://centers.iskcondesiretree.com/wp-content/uploads/2013/02/Sri-Sri-Gaura-Nitai.jpg',
          },
          {
            src: 'https://media-cdn.tripadvisor.com/media/photo-s/11/b8/fe/b6/srila-prabhupada-iskcon.jpg',
          },
        ],
      }
    },
  }
</script>