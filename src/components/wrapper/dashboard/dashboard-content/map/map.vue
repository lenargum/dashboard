<template>
  <div class="dashboard-container">
    <div class="map">
      <MapControl/>
      <div class="map__content">
        <MapSvg/>
      </div>
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
    flex-basis: 100%;
    height: 100%;
  }
}
</style>