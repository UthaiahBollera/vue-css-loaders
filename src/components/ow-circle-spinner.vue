

<template>
    <div :class="align">
      <div class="ow-spinner-container">      
        <div class="ow-spinner ow-circle-spinner"
         :class=[size,animDuration]
         ></div>
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
.center {
  text-align: center;
}
.left {
  text-align: left;
}
.right {
  text-align: right;
}

.ow-spinner-container {
  display: inline-block;
  position: relative;
}
.md {
  width: 100px;
  height: 100px;
}
.lg {
  width: 200px;
  height: 200px;
}
.sm {
  width: 50px;
  height: 50px;
}

.ow-spinner {
  border-radius: 100%;
  position: relative;
  margin: 0 auto;
}

.ow-circle-spinner:before,
.ow-circle-spinner:after {
  content: "";
  position: absolute;
  top: -10px;
  left: -10px;
  width: 100%;
  height: 100%;
  border-radius: 100%;
  border: 10px solid transparent;
  border-top-color: #3498db;
}
.slow:before {
  animation: spin 2s infinite !important;
}
.fast:before {
  animation: spin 0.5s infinite !important;
}
.medium:before {
  animation: spin 1s infinite !important;
}
.ow-circle-spinner:before {
  z-index: 100;
}

.ow-circle-spinner:after {
  border: 10px solid #ccc;
}

@keyframes spin {
  0% {
    -webkit-transform: rotate(0deg);
    -ms-transform: rotate(0deg);
    -o-transform: rotate(0deg);
    transform: rotate(0deg);
  }

  100% {
    -webkit-transform: rotate(360deg);
    -ms-transform: rotate(360deg);
    -o-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
</style>
