<template>
  <div class="nav-background">
    <div class="nav__menu-icon" v-on:click="closeMenu()">
      <svg width="15px" height="11px">
        <use href="map.svg#menu-icon_black"/>
      </svg>
    </div>
    <div class="nav-search-and-navbar">
      <SearchBar/>
      <NavBar/>
    </div>
  </div>
</template>

<script>
import SearchBar from "@/components/wrapper/dashboard/nav/nav-background/search-bar/search-bar";
import NavBar from "@/components/wrapper/dashboard/nav/nav-background/nav-bar/nav-bar";

export default {
  name: "NavBackground",
  components: {
    NavBar,
    SearchBar,
  },
  methods: {
    closeMenu() {
      var x = document.getElementById("drawer");
      if (x.style.display === "none") {
        x.style.display = "block";
      } else {
        x.style.display = "none";
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.nav-background {
  display: flex;
  flex-flow: row;
  align-items: center;
  justify-items: center;
  width: 100%;
  height: 60px;
  opacity: 0.9;

  background-color: #fff;
  -webkit-box-shadow: 0 0 18px rgba(17, 17, 17, .12);
  -moz-box-shadow: 0 0 18px rgba(17, 17, 17, .12);
  box-shadow: 0 0 18px rgba(17, 17, 17, .12);
}

.nav-search-and-navbar {
  display: flex;
  flex-flow: row;
  align-content: space-between;
  justify-content: center;
  width: -webkit-fill-available;
  height: 60px;
}

.nav__menu-icon {
  width: 60px;
  height: 60px;
  display: flex;
  flex-shrink: 0;
  justify-content: center;
  align-items: center;
}
</style>