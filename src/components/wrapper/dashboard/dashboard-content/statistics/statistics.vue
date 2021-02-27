<template>
  <div class="dashboard-container statistics">
    <div class="statistics-container">
      <div class="statistics-heading__icon">
        <CartIcon/>
      </div>
      <div class="statistics-heading">
        <h5>New Orders</h5>
        <div class="statistics-heading__arrow">
          <ArrowUpIcon/>
        </div>
        <div class="statistics-heading__percent-up">6.31%</div>
      </div>
      <div class="statistics__big-number">345</div>
      <div class="statistics__graph">
        <Graph1Svg/>
      </div>
    </div>
    <div class="statistics-container">
      <div class="statistics-heading__icon">
        <DollarIcon/>
      </div>
      <div class="statistics-heading">
        <h5>Total Revenue</h5>
        <div class="statistics-heading__arrow">
          <ArrowDownIcon/>
        </div>
        <div class="statistics-heading__percent-down">1.4%</div>
      </div>
      <div class="statistics__big-number">$25.534</div>
      <div class="statistics__graph">
        <Graph2Svg/>
      </div>
    </div>
    <div class="statistics-container">
      <div class="statistics-heading__icon">
        <FormIcon/>
      </div>
      <div class="statistics-heading">
        <h5>Task Complete</h5>
        <div class="statistics-heading__arrow">
          <ArrowDownIcon/>
        </div>
        <div class="statistics-heading__percent-down">0.7%</div>
      </div>
      <div class="statistics__big-number">123</div>
      <div class="statistics-vertical-graphs">
        <div class="statistics-vertical-graph">
          <div class="statistics-vertical-graph-header">
            <div class="statistics-vertical-graph-header__title">
              Today
            </div>
            <div class="statistics-vertical-graph-header__percent-today">
              67%
            </div>
          </div>
          <VerticalGraph1 class="statistics-vertical-graph__graph"/>
        </div>
        <div class="statistics-vertical-graph">
          <div class="statistics-vertical-graph-header">
            <div class="statistics-vertical-graph-header__title">
              Yesterday
            </div>
            <div class="statistics-vertical-graph-header__percent-yesterday">
              78%
            </div>
          </div>
          <VerticalGraph2 class="statistics-vertical-graph__graph"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ArrowUpIcon from "@/assets/img/content/statistics/arrows/arrow-up.svg"
import ArrowDownIcon from "@/assets/img/content/statistics/arrows/arrow-down.svg"
import CartIcon from "@/assets/img/content/statistics/icons/cart.svg"
import DollarIcon from "@/assets/img/content/statistics/icons/dollar.svg"
import FormIcon from "@/assets/img/content/statistics/icons/form.svg"
import Graph1Svg from "@/assets/img/content/statistics/graphs/graph1.svg"
import Graph2Svg from "@/assets/img/content/statistics/graphs/graph2.svg"
import VerticalGraph1 from "@/assets/img/content/statistics/vertical-graphs/vertical-graph1.svg"
import VerticalGraph2 from "@/assets/img/content/statistics/vertical-graphs/vertical-graph2.svg"

export default {
  name: "Statistics",
  components: {
    ArrowUpIcon,
    ArrowDownIcon,
    CartIcon,
    DollarIcon,
    FormIcon,
    Graph1Svg,
    Graph2Svg,
    VerticalGraph1,
    VerticalGraph2
  }
}
</script>

<style lang="scss" scoped>
.statistics {
  padding: 0;
  display: flex;
  flex-basis: 100%;
  flex-flow: row;

  &-container {
    display: flex;
    flex-flow: column nowrap;
    justify-items: flex-start;
    align-items: flex-start;
    flex-basis: 100%;
    height: min-content;
    padding: 22px 16px 22px 37px;
    position: relative;
  }

  .statistics-container + .statistics-container {
    height: auto;
    border-left: 1px solid #e7e7e7;
  }

  &-heading {
    position: relative;

    display: flex;
    flex-basis: 100%;
    flex-flow: row nowrap;
    gap: 8px;
    align-items: center;

    &__icon {
      display: flex;
      justify-content: center;
      align-items: center;

      position: absolute;
      top: 10%;
      right: 7%;
    }

    &__arrow {
    }

    &__percent {
      font-family: "Open Sans", sans-serif;
      font-size: 14.6px;
      font-weight: bold;
      font-stretch: normal;
      font-style: normal;
      line-height: 1;
      letter-spacing: normal;
      text-align: right;

      &-up {
        @extend .statistics-heading__percent;
        color: #2fad35;
      }

      &-down {
        @extend .statistics-heading__percent;
        color: #ff494a;
      }
    }
  }

  &__big-number {
    font-family: "Open Sans", sans-serif;
    font-size: 34px;
    font-weight: bold;
    font-stretch: normal;
    font-style: normal;
    line-height: 1.5;
    letter-spacing: normal;
    text-align: right;
    color: #313131;
  }

  &__graph {
    display: flex;
    justify-content: center;
    align-items: center;

    flex-basis: 100%;
    height: 100%;
  }

  &-vertical-graphs {
    display: flex;
    flex-flow: column;
    justify-content: center;

    flex-basis: 100%;
  }

  &-vertical-graph {
    &-header {
      display: flex;
      flex-flow: row nowrap;
      flex-shrink: 0;
      justify-content: space-between;

      &__title {
        font-family: 'Open Sans', sans-serif;
        font-size: 12px;
        font-weight: bold;
        font-stretch: normal;
        font-style: normal;
        letter-spacing: normal;
        color: #7b7b7b;
      }

      &__percent {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 3px 6px 3px 6px;
        border-radius: 11px;
        border: solid 1px;


        font-family: 'Open Sans', sans-serif;
        font-size: 9px;
        font-weight: bold;
        font-stretch: normal;
        font-style: normal;
        line-height: 1;
        letter-spacing: normal;

        &-today {
          @extend .statistics-vertical-graph-header__percent;
          color: #2abb9b;
        }

        &-yesterday {
          @extend .statistics-vertical-graph-header__percent;
          color: #4f80e1;
        }
      }
    }

    &__graph {
      flex-basis: 100%;
    }
  }
}
</style>