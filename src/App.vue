<template>
  <div id="app">
    <horizontal-barChart :data="chartData" :options="chartOptions"></horizontal-barChart>
  </div>
</template>

<script>
import horizontalBarChart from "./horizontalBarChart.js";
export default {
  name: "App",
  components: {
    "horizontal-barChart": horizontalBarChart
  },
  data() {
    return {
      chartData: {
        labels: ["Set data 1", "Set data 2", "Set data 3", "Set data 4"],
        datasets: [
          {
            label: "Low",
            data: [67.8, 73, 83, 17],
            backgroundColor: "#D6E9C6" // green
          },
          {
            label: "Moderate",
            data: [20.7, 61, 27, 75],
            backgroundColor: "#FAEBCC" // yellow
          },
          {
            label: "High",
            data: [11.4, 16, 71, 74],
            backgroundColor: "#EBCCD1" // red
          }
        ]
      },
      chartOptions: {
        scales: {
          xAxes: [
            {
              stacked: true
            }
          ],
          yAxes: [
            {
              stacked: true
            }
          ]
        }
      }
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
