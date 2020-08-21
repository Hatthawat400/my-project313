<template>
  <div id="app">
    <div>
      <slide />
    </div>
    <div class="row">
      <div class="col-md-6 mb-3">
        <img src="./assets/22.jpg" alt />
        <counter @cc="sum" />
      </div>
      <div class="col-md-6 mb-3 a">
        <h1>Totol = {{total}}</h1>
      </div>
    </div>
    <div class="row">
      <div class="col-md-6 mb-3">
        <img src="./assets/33.jpg" alt />
        <counter @bb="sumb" />
      </div>
      <div class="col-md-6 mb-3 a">
        <h1>Totol = {{tot}}</h1>
      </div>
    </div>
    <div class="row">
      <div class="col-md-6 mb-3">
        <img src="./assets/44.jpg" alt />
        <counter @dd="sumc" />
      </div>
      <div class="col-md-6 mb-3 a">
        <h1>Totol = {{tota}}</h1>
      </div>
    </div>
  </div>
</template>

<script>
import Counter from "./components/Counter";
import slide from "./components/slide";
export default {
  name: "App",
  components: {
    Counter,
    slide,
  },
  data: function () {
    return {
      total: 0, //ผลรวมทั้งหมด ---->เอาไปแสดงผล {{}}
      tot: 0,
      tota:0,
    };
  },

  methods: {
    sum(CounterValue) {
      this.total += CounterValue;
    },
    sumb(Value) {
      this.tot += Value;
    },
    sumc(Va) {
      this.tota += Va;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.a {
  height: 300px;
  margin: auto;
  margin-left: auto;
  margin-right: auto;
}
</style>
