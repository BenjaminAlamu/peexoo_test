<template>
  <div class="calendar">
    <div class="border p-2">
      <div class="calendar-header">
        <h4>{{month + ' - ' + year}}</h4>
      </div>
      <ul class="weekdays grid">
        <li v-for="(day, count) in days" class="inline px-3" :key="count">{{day}}</li>
      </ul>
      <ul class="dates grid">
        <li class="px-3" v-for="(blank, i) in firstDayOfMonth" :key="i">-</li>
        <li
          v-for="(date, index) in daysInMonth"
          class="px-3"
          :class="{'current-day': date == initialDate &amp;&amp; month == initialMonth && year == initialYear}"
          :key="index"
        >
          {{date}}
          <span></span>
          <br class="block" />
        </li>
      </ul>
    </div>
    <div class="mt-4">
      <i class="cursor-pointer fa fa-fw fa-chevron-left" @click="subtractMonth"></i>
      <i class="cursor-pointer fa fa-fw fa-chevron-right" @click="addMonth"></i>
    </div>
  </div>
</template>

<script>
import moment from "moment";
export default {
  data() {
    return {
      today: moment(),
      dateContext: moment(),
      days: ["Sun", "Mon", "Tue", "Wed", "Thur", "Fri", "Sat"]
    };
  },
  computed: {
    year: function() {
      var t = this;
      return t.dateContext.format("Y");
    },
    month: function() {
      var t = this;
      return t.dateContext.format("MMMM");
    },
    daysInMonth: function() {
      var t = this;
      return t.dateContext.daysInMonth();
    },
    currentDate: function() {
      var t = this;
      return t.dateContext.get("date");
    },
    firstDayOfMonth: function() {
      var t = this;
      var firstDay = moment(t.dateContext).subtract(t.currentDate - 1, "days");
      return firstDay.weekday();
    },
    initialDate: function() {
      var t = this;
      return t.today.get("date");
    },
    initialMonth: function() {
      var t = this;
      return t.today.format("MMMM");
    },
    initialYear: function() {
      var t = this;
      return t.today.format("Y");
    }
  },
  methods: {
    addMonth: function() {
      var t = this;
      t.dateContext = moment(t.dateContext).add(1, "month");
    },
    subtractMonth: function() {
      var t = this;
      t.dateContext = moment(t.dateContext).subtract(1, "month");
    }
  }
};
</script>

<style lang="css" scoped>
.dates,
.weekdays {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
}
</style>