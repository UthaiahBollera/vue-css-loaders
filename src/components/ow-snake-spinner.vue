

<template>
  <div :class="align">
      <div class="ow-spinner-container">    
      <div class="loader ow-snake-spinner" :class="animDuration">
          <span></span>
          <span></span>
          <span></span>
        </div>
        </div>
    </div>  
</template>

<script>
export default {
  props: {
    size: {
      type: String,
      default: "md"
    },
    align: {
      type: String,
      default: "left"
    },
    animDuration: {
      type: String,
      default: "medium"
    }
  },
  name: "loader"
};
</script>

<style scoped>
.ow-loader {
  width: 100px;
  height: 100px;
  border-radius: 100%;
  position: relative;
  margin: 0 auto;
}

.slow span:nth-child(1) {
  animation: bounce 2s ease-in-out infinite !important;
}

.slow span:nth-child(2) {
  animation: bounce 2s ease-in-out 0.5s infinite !important;
}

.slow span:nth-child(3) {
  animation: bounce 2s ease-in-out 1s infinite !important;
}

.ow-snake-spinner span {
  display: inline-block;
  width: 20px;
  height: 20px;
  border-radius: 100%;
  background-color: #3498db;
  margin: 35px 5px;
}

.ow-snake-spinner span:nth-child(1) {
  animation: bounce 1s ease-in-out infinite;
}

.ow-snake-spinner span:nth-child(2) {
  animation: bounce 1s ease-in-out 0.33s infinite;
}

.ow-snake-spinner span:nth-child(3) {
  animation: bounce 1s ease-in-out 0.66s infinite;
}

@keyframes bounce {
  0%,
  75%,
  100% {
    -webkit-transform: translateY(0);
    -ms-transform: translateY(0);
    -o-transform: translateY(0);
    transform: translateY(0);
  }

  25% {
    -webkit-transform: translateY(-20px);
    -ms-transform: translateY(-20px);
    -o-transform: translateY(-20px);
    transform: translateY(-20px);
  }
}
</style>
