<template>
  <div class="card bg-white border-0 rounded-3 mb-4">
    <div class="card-body p-4">
      <h3 class="mb-3">Billing Details</h3>
      <div class="d-flex align-items-center mb-2">
        <span class="text-secondary">Name:</span>
        <span class="ms-1">Gary Fraser</span>
      </div>
      <div class="d-flex align-items-center mb-2">
        <span class="text-secondary">Email:</span>
        <span class="ms-1">example@mail.com</span>
      </div>
      <div class="d-flex align-items-center mb-2">
        <span class="text-secondary">Phone:</span>
        <span class="ms-1">+1 444 333 5566</span>
      </div>
      <div class="d-flex mb-0">
        <span class="text-secondary">Address:</span>
        <span class="ms-1">715 Maple St, Hamletville, England</span>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "BillingDetails",
});
</script>
