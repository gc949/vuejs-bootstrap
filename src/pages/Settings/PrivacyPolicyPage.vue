<template>
  <div class="main-content-container overflow-hidden">
    <PageTitle pageTitle="Privacy Policy" subTitle="Settings" />

    <PrivacyPolicy />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PageTitle from "@/components/Common/PageTitle.vue";
import PrivacyPolicy from "@/components/Others/Settings/PrivacyPolicy/index.vue";

export default defineComponent({
  name: "PrivacyPolicyPage",
  components: {
    PageTitle,
    PrivacyPolicy,
  },
});
</script>
