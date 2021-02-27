<template>
  <div class="dashboard-container">
    <div class="map">
      <MapControl/>
      <div class="map__content">
        <svg width="873px" height="456px">
          <use href="map.svg#map-content"/>
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
import MapControl from "@/components/wrapper/dashboard/dashboard-content/map/map-control/map-control";

export default {
  name: "Map",
  components: {
    MapControl
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