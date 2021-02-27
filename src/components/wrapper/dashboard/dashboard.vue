<template>
  <div class="dashboard">
    <Nav/>
    <DashboardContent/>
  </div>
</template>

<script>
import Nav from "@/components/wrapper/dashboard/nav/nav";
import DashboardContent from "@/components/wrapper/dashboard/dashboard-content/dashboard-content";

export default {
  name: "Dashboard",
  components: {
    Nav,
    DashboardContent
  },
}
</script>

<style lang="scss" scoped>

</style>