<template>

    <v-card
      style="background-color: #121212"
      class="ma-2"
      height="300"
      max-width="200"
      @click="$router.push('/gameDetail')"
    >
      <v-img
        height="230"
        width="95%"
        :src="imageUrl"
        :elevation="2"
        :transition="{ 'transform': '0.2s ease-out' }"
        class="hoverable-image mr-auto ml-auto mt-1 cursor-pointer">
      </v-img>
      <v-card-text
        class="white--text pb-1 mt-auto">{{ title }}</v-card-text>
    </v-card>
</template>

<script>
export default {
  data(){
    return{
      hovering: false
    }
  },
  props: {
    imageUrl: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      default: ''
    }
  },
  methods: {
    onHover(){
      setTimeout(()=>{
          this.hovering = true
      },
      1500)
      this.hovering = false
    }
  }
}
</script>
<style scoped>
.hoverable-image:hover {
  transform: scale(1.1);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
}
</style>
