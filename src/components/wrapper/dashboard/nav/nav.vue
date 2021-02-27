<template>
<div class="nav">
  <NavBackground/>
</div>
</template>

<script>
import NavBackground from "@/components/wrapper/dashboard/nav/nav-background/nav-background";
export default {
  name: "nav",
  components: {NavBackground}
}
</script>

<style lang="scss" scoped>
.nav {
  width: 100%;
  height: 60px;
}
</style>