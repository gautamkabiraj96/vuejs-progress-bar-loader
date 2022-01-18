<template>
  <div id="app">
    <div class="np-progress-container">
      <div
        class="np-progress-loader"
        v-bind:style="'width:' + loadedPercentage + '%'"
      ></div>
    </div>
    <div>
      <div class="np-ib">
        <input
          class="np-input-number"
          type="number"
          v-model="loadedPercentage"
        />
      </div>
      <div class="np-ib">
        <div class="np-perc">%</div>
      </div>
    </div>
    <div class="np-credits">www.nightprogrammer.com</div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      loadedPercentage: 0,
    };
  },
  methods: {
    loadProgress() {
      this.loadedPercentage = 50;
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.np-ib {
  display: inline-block;
}
.np-progress-container {
  width: 500px;
  height: 50px;
  background: rgb(207, 207, 207);
  border-radius: 6px;
  position: relative;
}
.np-progress-loader {
  border-radius: 6px;
  background: rgb(37, 29, 176);
  background: linear-gradient(0deg, #251db0 0%, #227cb8 50%, #00d4ff 100%);
  height: 50px;
  width: 0%;
  max-width: 100%;
  min-width: 0%;
  overflow: hidden;
}
.np-input-number {
  outline: none;
  font-size: 20px;
  width: 100px;
  margin: 20px 0;
  border: 1px solid #c1d8e9;
  border-radius: 4px;
  background: #e9f6ff;
  padding: 4px;
}
.np-perc {
  font-size: 24px;
  padding-left: 10px;
}
.np-credits {
  font-size: 12px;
}
</style>