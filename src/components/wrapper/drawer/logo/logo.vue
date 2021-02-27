<template>
  <div class="logo">
    <div class="logo__top_lines">
      <svg width="52px" height="6px">
        <use href="map.svg#top_lines"/>
      </svg>
    </div>
    <div class="logo__title">ADS</div>
    <div class="logo__version">V2.00</div>
    <div class="logo__bottom_lines">
      <svg width="53px" height="5px">
        <use href="map.svg#bottom_lines"/>
      </svg>
    </div>
  </div>
</template>

<script>


export default {
  name: "Logo",
  components: {}
}
</script>

<style lang="scss" scoped>
.logo {
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;

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