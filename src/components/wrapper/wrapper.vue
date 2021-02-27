<template>
  <div class="wrapper">
    <Drawer/>
    <Dashboard/>
  </div>
</template>

<script>
import Drawer from "@/components/wrapper/drawer/drawer";
import Dashboard from "@/components/wrapper/dashboard/dashboard";

export default {
  name: "Wrapper",
  components: {Dashboard, Drawer}
}
</script>

<style lang="scss" scoped>
.wrapper {
  display: flex;
  width: 100%;
  -webkit-flex-flow: row nowrap;
  flex-flow: row nowrap;
  align-content: center;
  justify-content: flex-start;

}
$drawer-width: 61px;
.drawer {
  background-color: #313131;
  height: 100%;
  width: $drawer-width;
}
.dashboard {
  width: calc(100% - #{$drawer-width});
  height: 100%;
}
</style>