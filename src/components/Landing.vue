<template>
  <div >
    <v-container>
      <v-row class="container">
        <v-col cols="12">
          <div align="center">
            <h1 class="title-scramble" ref="title">Quick think of something smart</h1>
            <h3 class="subtitle-scramble" ref="subtitle">Ummmmmmmmm.....</h3>
          </div>

        </v-col>
      </v-row>
    </v-container>
    <gallery />



  </div>
</template>

<script>
import gallery from './Gallery.vue'

export default {
  name: 'Landing',
  mounted() {
    setTimeout(() => {
      this.$refs.title.innerText = "Dedicated to good times, and Jason";
      this.$refs.subtitle.innerText = "And hot chocolate of course....";
    }, 2000);
  }
}

</script>

<style scoped>

.container {
  border-radius: 8px;
  margin: 45px;
  width: 100%;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  animation: scramble 3s;
  animation-delay: 0.6s;
}

.title-scramble {
  animation: scramble 2s;
  font-size: 24px;
  font-weight: bold;
  color: black;
}

.subtitle-scramble {
  animation: scramble 2s;
  animation-delay: 0.225s;
  font-size: 18px;
  color: #666;
}

@keyframes scramble {
  0% {
    transform: translateX(0);
    color: red;
  }
  25% {
    transform: translateX(-10px);
  }
  50% {
    transform: translateX(15px);
    color: purple;
  }
  75% {
    transform: translateX(-5px);
  }
  100% {
    transform: translateX(0);
    color: yellow;
  }
}
</style>



