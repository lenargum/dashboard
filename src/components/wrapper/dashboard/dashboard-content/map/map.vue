<template>
  <div class="dashboard-container map">
    <MapControl/>
    <div class="map__content">
      <MapSvg/>
    </div>
  </div>
</template>

<script>
import MapControl from "@/components/wrapper/dashboard/dashboard-content/map/map-control/map-control";
import MapSvg from "@/assets/img/content/map/map-content.svg"

export default {
  name: "Map",
  components: {
    MapControl,
    MapSvg
  }
}
</script>

<style lang="scss" scoped>
.map {

  &__content {
    width: 100%;
    height: 100%;
  }
}
</style>