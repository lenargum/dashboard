<template>
  <div class="drawer" id="drawer">
    <Logo/>
    <DrawerProfile/>
    <MenuIcon/>
    <MenuSections/>
  </div>
</template>

<script>
import Logo from "@/components/wrapper/drawer/logo/logo";
import DrawerProfile from "@/components/wrapper/drawer/drawer-profile/drawer-profile"
import MenuIcon from "@/components/wrapper/drawer/menu-icon/menu-icon";
import MenuSections from "@/components/wrapper/drawer/menu-sections/menu-sections";

export default {
  name: "Drawer",
  components: {
    Logo,
    DrawerProfile,
    MenuIcon,
    MenuSections
  }
}
</script>

<style scoped>

</style>