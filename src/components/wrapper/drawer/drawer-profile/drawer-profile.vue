<template>
  <div class="drawer-profile">
    <div class="avatar">
      <img class="avatar avatar__pic"
           src="@/assets/img/drawer/drawer-profile/stub-man.png" alt="">
      <svg class="avatar avatar__status" width="37px" height="39px">
        <use href="map.svg#avatar_status"/>
      </svg>
    </div>
    <div class="drawer-profile__initials">MJ</div>
    <div class="drawer-profile__position">Graphic Designer</div>
  </div>
</template>

<script>


export default {
  name: "DrawerProfile",
  components: {},
}
</script>

<style lang="scss" scoped>
.drawer-profile {
  display: flex;
  flex-flow: column;
  height: auto;
  width: auto;
  margin: 73px 0 49px;

  align-items: center;
  justify-content: center;

  &__initials {
    width: min-content;
    height: min-content;
    padding: 9px 0;
    font-family: 'OpenSans', sans-serif;
    font-size: 14px;
    font-weight: bold;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: normal;
    text-align: center;
    color: #ffffff;
  }

  &__position {
    word-break: break-word;
    font-family: 'OpenSans', sans-serif;
    font-size: 12px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: 10.08pt;
    letter-spacing: normal;
    text-align: center;
    color: #7c7c7c;
  }
}

.avatar {
  display: flex;
  justify-content: center;
  align-items: center;

  width: 37px;
  height: 39px;

  &__pic {
    //mask: var(--mask-src) no-repeat center / contain;
    //-webkit-mask-position: center;
    //-webkit-mask-size: 100% 100%;
  }

  &__status {
    position: absolute;
  }
}
</style>