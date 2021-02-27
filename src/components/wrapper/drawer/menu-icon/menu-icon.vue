<template>
  <div class="menu-icon">
    <div class="menu-icon__background">
      <MenuIconSvg class="menu-icon__icon" />
    </div>
    <div class="menu-icon__underline"></div>
  </div>
</template>

<script>
import MenuIconSvg from "@/assets/img/drawer/menu-icon/icon.svg"

export default {
  name: "MenuIcon",
  components: {
    MenuIconSvg
  }
}
</script>

<style lang="scss" scoped>
.menu-icon {
  &__background {
    display: flex;
    align-items: center;
    justify-content: center;

    width: 62px;
    height: 42px;
    background-color: #181818;
  }

  &__icon {
    width: 15px;
    height: 11px;
  }

  //todo: replace to :after
  &__underline {
    width: 62px;
    height: 3px;
    background-color: #101010;
  }
}
</style>