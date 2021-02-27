<template>
  <div class="menu-sections">
    <div class="menu-section">
      <div class="menu-section__title">MAIN</div>
      <div class="menu-items">
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="16px" height="15px">
            <use href="map.svg#dashboard"/>
          </svg>
        </div>
        <div class="menu-item menu-item_active">
          <svg class="menu-section__menu-icon" width="19px" height="19px">
            <use href="map.svg#brush"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="18px" height="18px">
            <use href="map.svg#palette"/>
          </svg>
        </div>
      </div>
    </div>
    <div class="menu-section">
      <div class="menu-section__title">COMP</div>
      <div class="menu-items">
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="12px" height="12px">
            <use href="map.svg#4squares"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="15px" height="16px">
            <use href="map.svg#editors"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="16px" height="14px">
            <use href="map.svg#table"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="11px" height="13px">
            <use href="map.svg#play"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon_stroke-only" width="16.5px" height="16.5px">
            <use href="map.svg#forms"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="15px" height="15px">
            <use href="map.svg#smile"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="17px" height="15px">
            <use href="map.svg#upload"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="15px" height="15px">
            <use href="map.svg#info"/>
          </svg>
        </div>
      </div>
    </div>
    <div class="menu-section">
      <div class="menu-section__title">DATA</div>
      <div class="menu-items">
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="17px" height="17px">
            <use href="map.svg#graph"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="20px" height="17px">
            <use href="map.svg#location"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="22px" height="19px">
            <use href="map.svg#charts"/>
          </svg>
        </div>
      </div>
    </div>
    <div class="menu-section">
      <div class="menu-section__title">PAGES</div>
      <div class="menu-items">
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="15px" height="13px">
            <use href="map.svg#warning"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="18px" height="20px">
            <use href="map.svg#login"/>
          </svg>
        </div>
        <div class="menu-item">
          <svg class="menu-section__menu-icon" width="16px" height="15px">
            <use href="map.svg#display"/>
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MenuSections",
  components: {},
}
</script>

<style lang="scss" scoped>
.menu-sections {
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-items: center;

  padding: 0 0 30px;
}

.menu-section {
  width: 100%;
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-items: center;

  padding: 7px 0 7px;

  &__title {
    width: min-content;
    height: min-content;
    font-family: 'OpenSans', sans-serif;
    font-size: 11px;
    font-weight: bold;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: normal;
    text-align: right;
    color: #909090;

    padding: 15px 0 15px;
  }

  &__menu-icon {
    text-align: center;
    fill: rgb(193, 193, 193);

    &_stroke-only {
      text-align: center;
      stroke: rgb(193, 193, 193);
      fill: none;
    }
  }
}

.menu-items {
  display: flex;
  flex-flow: column;
  width: 100%;
  height: auto;

  &::before {
    content: "";
    height: 1px;
    width: 50%;
    background-color: yellow;
  }
}

.menu-item {
  display: flex;
  width: 100%;
  height: 61px;
  align-items: center;
  justify-content: center;

  &_active {
    background-color: #5F5F5F;
  }

  &:hover {
    background-color: yellow;
    cursor: pointer;
  }

  &:hover .child {
    color: red;
  }
}

.menu-item:hover .menu-section__menu-icon {
  fill: red;
}

.menu-item:hover .menu-section__menu-icon_stroke-only {
  stroke: red;
}
</style>