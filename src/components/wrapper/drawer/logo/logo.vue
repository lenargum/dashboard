<template>
  <div class="logo">
    <div class="logo__top_lines">
      <LogoTopLines/>
    </div>
    <div class="logo__title">ADS</div>
    <div class="logo__version">V2.00</div>
    <div class="logo__bottom_lines">
      <LogoBottomLines/>
    </div>
  </div>
</template>

<script>
import LogoTopLines from "@/assets/img/drawer/logo/top_lines.svg"
import LogoBottomLines from "@/assets/img/drawer/logo/bottom_lines.svg"


export default {
  name: "Logo",
  components: {
    LogoTopLines,
    LogoBottomLines
  }
}
</script>

<style lang="scss" scoped>
.logo {
  display: flex;
  flex-flow: column;
  height: auto;
  width: auto;

  background-color: transparent;
  margin: 7px 0 7px;

  &__top_lines {
    display: flex;
    flex-shrink: 0;

    width: 52px;
    padding: 0 7px 0 2px;
  }

  &__title {
    padding: 4px 9px 0 13px;
    font-family: 'Montserrat', sans-serif;
    font-size: 17px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: 1.7px;
    text-align: left;
    color: #ffffff;
  }

  &__version {
    padding: 4px 13px 4px 15px;
    font-family: 'Montserrat', sans-serif;
    font-size: 10px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: 1px;
    text-align: left;
    color: #ff6a6a;
  }

  &__bottom_lines {
    display: flex;
    flex-shrink: 0;

    width: 53px;
    padding: 0 4px;
  }
}
</style>