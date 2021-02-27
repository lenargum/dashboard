<template>
  <div class="menu-sections">
    <div class="menu-section">
      <div class="menu-section__title">MAIN</div>
      <div class="menu-items">
        <div class="menu-item">
          <DashboardIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item menu-item_active">
          <BrushIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <PaletteIcon class="menu-section__menu-icon"/>
        </div>
      </div>
    </div>
    <div class="menu-section">
      <div class="menu-section__title">COMP</div>
      <div class="menu-items">
        <div class="menu-item">
          <FourSquaresIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <EditorsIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <TableIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <PlayIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <FormsIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <SmileIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <UploadIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <InfoIcon class="menu-section__menu-icon"/>
        </div>
      </div>
    </div>
    <div class="menu-section">
      <div class="menu-section__title">DATA</div>
      <div class="menu-items">
        <div class="menu-item">
          <GraphIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <LocationIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <ChartsIcon class="menu-section__menu-icon"/>
        </div>
      </div>
    </div>
    <div class="menu-section">
      <div class="menu-section__title">PAGES</div>
      <div class="menu-items">
        <div class="menu-item">
          <WarningIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <LoginIcon class="menu-section__menu-icon"/>
        </div>
        <div class="menu-item">
          <DisplayIcon class="menu-section__menu-icon"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import DashboardIcon from "@/assets/img/drawer/menu-sections/main/dashboard.svg"
import BrushIcon from "@/assets/img/drawer/menu-sections/main/brush.svg"
import PaletteIcon from "@/assets/img/drawer/menu-sections/main/palette.svg"

import FourSquaresIcon from "@/assets/img/drawer/menu-sections/comp/4squares.svg"
import EditorsIcon from "@/assets/img/drawer/menu-sections/comp/editors.svg"
import TableIcon from "@/assets/img/drawer/menu-sections/comp/table.svg"
import PlayIcon from "@/assets/img/drawer/menu-sections/comp/play.svg"
import FormsIcon from "@/assets/img/drawer/menu-sections/comp/forms.svg"
import SmileIcon from "@/assets/img/drawer/menu-sections/comp/smile.svg"
import UploadIcon from "@/assets/img/drawer/menu-sections/comp/upload.svg"
import InfoIcon from "@/assets/img/drawer/menu-sections/comp/info.svg"

import GraphIcon from "@/assets/img/drawer/menu-sections/data/graph.svg"
import LocationIcon from "@/assets/img/drawer/menu-sections/data/location.svg"
import ChartsIcon from "@/assets/img/drawer/menu-sections/data/charts.svg"

import WarningIcon from "@/assets/img/drawer/menu-sections/pages/warning.svg"
import LoginIcon from "@/assets/img/drawer/menu-sections/pages/login.svg"
import DisplayIcon from "@/assets/img/drawer/menu-sections/pages/display.svg"


export default {
  name: "MenuSections",
  components: {
    DashboardIcon,
    BrushIcon,
    PaletteIcon,
    FourSquaresIcon,
    EditorsIcon,
    TableIcon,
    PlayIcon,
    FormsIcon,
    SmileIcon,
    UploadIcon,
    InfoIcon,
    GraphIcon,
    LocationIcon,
    ChartsIcon,
    WarningIcon,
    LoginIcon,
    DisplayIcon
  },
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

  &:hover .child{
    color: red;
  }
}

.menu-section__menu-icon {
  text-align: center;
  fill: rgb(193, 193, 193);
  width: auto;
  height: auto;
}

.menu-item:hover .menu-section__menu-icon{
  fill: red;
}
</style>