<template>
  <div class="nav-bar">
    <div class="nav-bar-menu-item">
      <PowerIcon/>
      <div class="nav-bar-menu-item-dropdown">
        <div class="nav-bar-menu-item-dropdown__item span">
          Profile
        </div>
        <div class="nav-bar-menu-item-dropdown__item span">
          Log out
        </div>
      </div>
    </div>
    <div class="nav-bar-menu-item">
      <SettingIcon/>
      <SettingNotificationBadge class="nav-bar-menu-item_notification-badge"/>
    </div>
    <div class="nav-bar-menu-item">
      <ChatIcon/>
      <ChatNotificationBadge class="nav-bar-menu-item_notification-badge"/>
    </div>
    <div class="nav-bar-menu-item">
      <NotificationIcon/>
      <NotificationNotificationBadge class="nav-bar-menu-item_notification-badge"/>
    </div>
    <div class="nav-bar-menu-item">
      <FullscreenIcon/>
    </div>
  </div>
</template>

<script>
import PowerIcon from "@/assets/img/nav/nav-bar-icons/power.svg"
import SettingIcon from "@/assets/img/nav/nav-bar-icons/setting.svg"
import SettingNotificationBadge from "@/assets/img/nav/nav-bar-icons/setting-notification-badge.svg"
import ChatIcon from "@/assets/img/nav/nav-bar-icons/chat.svg"
import ChatNotificationBadge from "@/assets/img/nav/nav-bar-icons/chat-notification-badge.svg"
import NotificationIcon from "@/assets/img/nav/nav-bar-icons/notification.svg"
import NotificationNotificationBadge from "@/assets/img/nav/nav-bar-icons/notification-notification-badge.svg"
import FullscreenIcon from "@/assets/img/nav/nav-bar-icons/fullscreen.svg"

// todo: crop icons and notification badges to make them look more centered

export default {
  name: "NavBar",
  components: {
    PowerIcon,
    SettingIcon,
    SettingNotificationBadge,
    ChatIcon,
    ChatNotificationBadge,
    NotificationIcon,
    NotificationNotificationBadge,
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

    &_notification-badge {
      position: absolute;
    }

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

      &__item {
        padding: 3px 3px;

        &:hover {
          background-color: #DCDCDC;
        }
      }
    }

    &:hover &-dropdown {
      display: inline;
    }
  }
}
</style>