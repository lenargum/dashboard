<template>
  <div class="dashboard-content">
    <DashboardTitle/>
    <Map/>
    <Statistics/>
  </div>
</template>

<script>
import DashboardTitle from "@/components/wrapper/dashboard/dashboard-content/dashboard__title";
import Map from "@/components/wrapper/dashboard/dashboard-content/map/map";
import Statistics from "@/components/wrapper/dashboard/dashboard-content/statistics/statistics";

export default {
  name: "DashboardContent",
  components: {
    Statistics,
    Map,
    DashboardTitle
  }
}
</script>

<style lang="scss">
.dashboard-container {
  display: flex;
  flex-flow: column;
  width: -webkit-fill-available;
  height: min-content;
  padding: 16px 40px 32px 40px;
  border-bottom: 1px solid #e7e7e7;
}

.dashboard-content {
  display: flex;
  flex-basis: 100%;

  height: 100%;
  flex-flow: column;
  justify-items: flex-start;
  align-items: flex-start;
}
</style>