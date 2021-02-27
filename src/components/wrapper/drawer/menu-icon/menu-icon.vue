<template>
  <div class="menu-icon">
    <div class="menu-icon__background">
      <svg width="15px" height="11px">
        <use href="map.svg#menu-icon"/>
      </svg>
    </div>
    <div class="menu-icon__underline"></div>
  </div>
</template>

<script>

export default {
  name: "MenuIcon",
  components: {}
}
</script>

<style lang="scss" scoped>
.menu-icon {
  &__background {
    display: flex;
    align-items: center;
    justify-content: center;

    width: calc(100% + 1px);
    height: 42px;
    background-color: #181818;
  }

  //todo: replace to :after
  &__underline {
    height: 3px;
    background-color: #101010;
  }
}
</style>