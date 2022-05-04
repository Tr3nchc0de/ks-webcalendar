
<template>
  <div class="hello">
    <h1>Calendar</h1>

    <!-- <button v-on:click="getWeatherData">Get Weather Data</button> -->
    <!-- <div>{{weatherDataList}}</div> -->
   <div v-for="calendarData in calendarDataList" :key="calendarData" class="calendar-data">
      {{Pager}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'WebCalendar',
  data() {
    return {
      calendarDataList: [],
      EventOverview: [],
      Pager: []
    };
  },
  methods: {  
    getCalendarData() {   
      fetch("calendar.json")
        .then(response => response.json())
        .then(data => (this.calendarDataList = data));
    }
  },
  beforeMount(){
    this.getCalendarData()
 },

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

