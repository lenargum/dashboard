<template>
  <div class="search-bar">
    <div class="search-bar__icon">
      <svg width="12px" height="12px">
        <use href="map.svg#magnifier"/>
      </svg>
    </div>
    <input class="search-bar__text-field" type="text" placeholder="Search Something...">
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  components: {}
}
</script>

<style lang="scss" scoped>
.search-bar {
  display: flex;
  flex-shrink: 0;
  flex-flow: row-reverse nowrap;
  justify-content: flex-start;
  align-items: center;
  flex-basis: 100%;
  max-width: 250px;
  -webkit-border-radius: 20px;
  -moz-border-radius: 20px;
  border-radius: 20px;

  margin: 13px 12px 14px 12px;
  padding: 0 15px 0 17px;

  border: solid 1px #cccccc;
  background-color: #fff;
  overflow: hidden;

  &__icon {
    display: flex;
    flex-shrink: 1;
    justify-content: center;
    align-items: center;
    height: 100%;

    &:hover {
      cursor: pointer;
    }
  }

  &__text-field {
    flex-basis: 100%;
    height: 100%;

    display: flex;
    flex-flow: row nowrap;
    justify-items: flex-start;
    align-items: center;
    font-family: "Open Sans", sans-serif;
    font-size: 13px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: 1.2;
    letter-spacing: normal;
    text-align: left;
    color: #1F1F1F;
    border: none;
    padding: 1px 2px;

    &:focus {
      outline: none;
    }

    &::placeholder {
      font-family: "Open Sans", sans-serif;
      font-size: 13px;
      font-weight: normal;
      font-stretch: normal;
      font-style: normal;
      //line-height: 1.2;
      letter-spacing: normal;
      text-align: left;
      color: #8b8b8b;
    }
  }
}
</style>