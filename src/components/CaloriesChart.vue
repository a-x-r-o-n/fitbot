<template>
  <div class="bg-gray-800 p-4 md:p-6 rounded-xl shadow-lg w-full h-64 md:h-80">
    <Line :data="chartData" :options="chartOptions" />
  </div>
</template>

<script setup>
import { Line } from 'vue-chartjs'
import {
  Chart as ChartJS,
  LineElement,
  CategoryScale,
  LinearScale,
  PointElement,
  Tooltip
} from 'chart.js'

ChartJS.register(LineElement, CategoryScale, LinearScale, PointElement, Tooltip)

const chartData = {
  labels: [
    'W-1', 'W-2', 'W-3', 'W-4', 'W-5', 'W-6', 'W-7', 'W-8',
    'W-9', 'W-10', 'W-11', 'W-12', 'W-13', 'W-14', 'W-15',
    'W-16', 'W-17', 'W-18'
  ],
  datasets: [{
    label: 'Calories',
    data: [
      3000, 3200, 3100, 2900,  // Week 1
      4500, 4300, 4400, 4600,  // Week 2
      4000, 3900, 4100, 4200,  // Week 3
      4778, 4900, 4800, 4700,  // Week 4
      5000, 5100, 5200, 4950,  // Week 5
      4800, 4700, 4900, 5100,  // Week 6
      5300, 5200, 5400, 5500,  // Week 7
      5600, 5500, 5700, 5800,  // Week 8
      5900, 6000, 6100, 5950,  // Week 9
      5800, 5700, 5900, 6100,  // Week 10
      5200, 5300, 5400, 5500,  // Week 11
      5600, 5700, 5800, 5900,  // Week 12
      6000, 6100, 6200, 6150,  // Week 13
      6300, 6400, 6500, 6600,  // Week 14
      6700, 6800, 6900, 7000,  // Week 15
      7100, 7200, 7300, 7250,  // Week 16
      7400, 7500, 7600, 7700   // Week 17
    ],
    fill: true,
    backgroundColor: 'rgba(255,255,0,0.1)',
    borderColor: '#FFE600',
    tension: 0.3
  }]
}

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  plugins: {
    legend: { display: false }
  },
  scales: {
    x: { ticks: { color: '#fff' } },
    y: { ticks: { color: '#fff' } }
  }
}
</script>
