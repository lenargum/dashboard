<template>
  <div class="nav-bar">
    <div class="nav-bar-menu-item">
      <PowerIcon />
      <div class="nav-bar-menu-item-dropdown">
        <span>Log out</span>
      </div>
    </div>
    <div class="nav-bar-menu-item">
      <SettingIcon />
    </div>
    <div class="nav-bar-menu-item">
      <ChatIcon />
    </div>
    <div class="nav-bar-menu-item">
      <NotificationIcon />
    </div>
    <div class="nav-bar-menu-item">
      <FullscreenIcon />
    </div>
  </div>
</template>

<script>
import PowerIcon from "@/assets/img/nav/nav-bar-icons/power.svg"
import SettingIcon from "@/assets/img/nav/nav-bar-icons/setting.svg"
import ChatIcon from "@/assets/img/nav/nav-bar-icons/chat.svg"
import NotificationIcon from "@/assets/img/nav/nav-bar-icons/notification.svg"
import FullscreenIcon from "@/assets/img/nav/nav-bar-icons/fullscreen.svg"


export default {
  name: "NavBar",
  components: {
    PowerIcon,
    SettingIcon,
    ChatIcon,
    NotificationIcon,
    FullscreenIcon
  }
}
</script>

<style lang="scss" scoped>
.nav-bar {
  width: 100%;
  height: 100%;
  display: flex;
  flex-flow: row-reverse nowrap;
  justify-items: start;
  align-items: center;
  column-gap: 35px;
  padding: 0 35px 0;

  &-menu-item {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;

    width: 30px;
    height: 30px;

    &:hover {
      cursor: pointer;
    }

    &-dropdown {
      display: none;
      position: absolute;

      font-family: "Open Sans", sans-serif;

      top: 50%;
      right: 10%;
      padding: 16px;
      min-width: 160px;

      background-color: #f5f5f5;

      -webkit-box-shadow: 0 0 18px rgba(17, 17, 17, .12);
      -moz-box-shadow: 0 0 18px rgba(17, 17, 17, .12);
      box-shadow: 0 0 18px rgba(17, 17, 17, .12);

      border-radius: 5px;

      border: solid 1px #cccccc;
      z-index: 1;
    }

    &:hover &-dropdown {
      display: inline;
    }
  }
}
</style>