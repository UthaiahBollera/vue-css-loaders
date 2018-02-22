<template>
  <div id="app">    
  <div className="clear50"></div>
    <CircleSpinner size="sm"
     align="right"
     animDuration="medium" />
     <div className="clear50"></div>

     <SnakeSpinner size="sm"
     align="center"
     animDuration="medium" />
     
  </div>
</template>

<script>
import { CircleSpinner, SnakeSpinner } from "./components/index";

export default {
  name: "App",
  components: {
    CircleSpinner,
    SnakeSpinner
  }
};
</script>

<style>
.clear50 {
  margin-top: 50px;
}
</style>
