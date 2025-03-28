<script setup>
import { ref, onMounted } from 'vue'

const time = ref('')
const days = ['Zo', 'Ma', 'Di', 'Wo', 'Do', 'Vr', 'Za']
const months = ['jan', 'feb', 'mrt', 'apr', 'mei', 'jun', 'jul', 'aug', 'sep', 'okt', 'nov', 'dec']

function updateTime() {
  const now = new Date()
  const day = days[now.getDay()]
  const date = now.getDate()
  const month = months[now.getMonth()]
  const hours = String(now.getHours()).padStart(2, '0')
  const minutes = String(now.getMinutes()).padStart(2, '0')
  time.value = `${day} ${date} ${month} ${hours}:${minutes}`
}


// Update the time immediately and set an interval to update it every minute
onMounted(() => {
  updateTime()
  setInterval(updateTime, 60000)
})
</script>

<template>
  <div class="time">{{ time }}</div>
</template>



