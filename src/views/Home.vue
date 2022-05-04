<template>
  <div class="home">
   
   <WebCalendar/>
  </div>
</template>

<script>
// @ is an alias to /src
import WebCalendar from '@/components/WebCalendar.vue'

export default {
  name: 'Home',
  components: {
    WebCalendar
  }
}
</script>
