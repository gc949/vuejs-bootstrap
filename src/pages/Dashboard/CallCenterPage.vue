<template>
  <div class="main-content-container overflow-hidden">
    <div class="row">
      <div class="col-xxl-8">
        <Overview />
      </div>
      <div class="col-xxl-4">
        <div class="row">
          <div class="col-xxl-12 col-md-6">
            <InboundCallsChart />
          </div>
          <div class="col-xxl-12 col-md-6">
            <OutboundCallsChart />
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-lg-7 col-xxl-6">
        <AgentsPerformanceOverview />
      </div>
      <div class="col-lg-5 col-xxl-6">
        <CallCenterGeography />
      </div>
    </div>
    <div class="row">
      <div class="col-xxl-4">
        <AgentAvgEarnings />
      </div>
      <div class="col-xxl-8">
        <RecentCalls />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, onMounted, onBeforeUnmount } from "vue";
import Overview from "../../components/Dashboard/CallCenter/Overview/index.vue";
import InboundCallsChart from "../../components/Dashboard/CallCenter/InboundCallsChart.vue";
import OutboundCallsChart from "../../components/Dashboard/CallCenter/OutboundCallsChart.vue";
import AgentsPerformanceOverview from "../../components/Dashboard/CallCenter/AgentsPerformanceOverview.vue";
import CallCenterGeography from "../../components/Dashboard/CallCenter/CallCenterGeography.vue";
import AgentAvgEarnings from "../../components/Dashboard/CallCenter/AgentAvgEarnings/index.vue";
import RecentCalls from "../../components/Dashboard/CallCenter/RecentCalls.vue";

export default defineComponent({
  name: "CallCenterPage",
  components: {
    Overview,
    InboundCallsChart,
    OutboundCallsChart,
    AgentsPerformanceOverview,
    CallCenterGeography,
    AgentAvgEarnings,
    RecentCalls,
  },
  setup() {
    onMounted(() => {
      document.body.classList.add("bg-white");
    });

    onBeforeUnmount(() => {
      document.body.classList.remove("bg-white");
    });
  },
});
</script>

<style lang="scss">
body {
  &.bg-white {
    .sidebar-area {
      border-right: var(--bs-border-width) var(--bs-border-style)
        var(--bs-border-color) !important;
    }
    .header-area {
      padding: 12px 0 !important;
      &.sticky {
        padding-left: 25px !important;
        padding-right: 25px !important;
      }
      &.mb-4 {
        margin-bottom: 0.5rem !important;
      }
    }
    .footer-area {
      border: var(--bs-border-width) var(--bs-border-style)
        var(--bs-border-color) !important;
    }
  }
}
</style>
