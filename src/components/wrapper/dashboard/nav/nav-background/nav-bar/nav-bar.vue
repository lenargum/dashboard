<template>
  <div class="nav-bar">
    <div class="nav-bar-menu-item">
      <svg width="14px" height="15px">
        <use href="map.svg#power"/>
      </svg>
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
      <svg width="29px" height="32px">
        <use href="map.svg#setting"/>
      </svg>
      <svg width="29px" height="32px" class="nav-bar-menu-item_notification-badge">
        <use href="map.svg#setting-notification-badge"/>
      </svg>
    </div>
    <div class="nav-bar-menu-item">
      <svg width="30px" height="26px">
        <use href="map.svg#chat"/>
      </svg>
      <svg width="30px" height="26px" class="nav-bar-menu-item_notification-badge">
        <use href="map.svg#chat-notification-badge"/>
      </svg>
    </div>
    <div class="nav-bar-menu-item">
      <svg width="27px" height="28px">
        <use href="map.svg#notification"/>
      </svg>
      <svg width="27px" height="28px" class="nav-bar-menu-item_notification-badge">
        <use href="map.svg#notification-notification-badge"/>
      </svg>
    </div>
    <div class="nav-bar-menu-item">
      <svg width="16px" height="16px">
        <use href="map.svg#fullscreen"/>
      </svg>
    </div>
  </div>
</template>

<script>
// todo: crop icons and notification badges to make them look more centered

export default {
  name: "NavBar",
  components: {}
}
</script>

<style lang="scss" scoped>
.nav-bar {
  display: flex;
  flex-basis: 100%;
  height: 100%;
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