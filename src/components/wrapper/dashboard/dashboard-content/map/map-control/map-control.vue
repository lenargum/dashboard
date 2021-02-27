<template>
  <div class="map-control">
    <div class="map-control-container">
      <PlusSignIcon/>
    </div>
    <div class="map-control-container">
      <MinusSignIcon/>
    </div>
  </div>
</template>

<script>
import PlusSignIcon from "@/assets/img/content/map/control/plus-sign.svg"
import MinusSignIcon from "@/assets/img/content/map/control/minus-sign.svg"

export default {
  name: "MapControl",
  components: {
    PlusSignIcon,
    MinusSignIcon
  }
}
</script>

<style lang="scss" scoped>
.map-control {
  position: absolute;

  display: flex;
  flex-flow: column;
  width: 41px;
  border: solid 1px #cccccc;
  background-color: rgba(255, 255, 255, 0.5);

  &-container {
    display: flex;
    width: 41px;
    height: 41px;
    align-items: center;
    justify-content: center;

    &:hover {
      background-color: rgba(229, 229, 229, 0.5);
      cursor: pointer;
    }
  }

  .map-control-container + .map-control-container {
    border-top: solid 1px #cccccc;
  }
}

</style>