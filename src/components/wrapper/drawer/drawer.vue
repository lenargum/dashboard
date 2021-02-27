<template>
  <div class="drawer">
    <Logo/>
    <DrawerProfile/>
    <MenuIcon/>
    <MenuSections/>
  </div>
</template>

<script>
import DrawerProfile from "@/components/wrapper/drawer/drawer-profile/drawer-profile"
import Logo from "@/components/wrapper/drawer/logo/logo";
import MenuIcon from "@/components/wrapper/drawer/menu-icon/menu-icon";
import MenuSections from "@/components/wrapper/drawer/menu-sections/menu-sections";

export default {
  name: "Drawer",
  components: {
    MenuSections,
    MenuIcon,
    Logo,
    DrawerProfile
  }
}
</script>

<style scoped>

</style>