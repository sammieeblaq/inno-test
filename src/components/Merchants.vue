<template>
  <div>
    <div class="container">
      <div class="mt-4">
        <div>
          <div>
            <h3>Merchants</h3>
          </div>
          <div class="d-flex">
            <h5 class="text-secondary mr-4 sub__header" @click="method">All</h5>
            <h5 class="text-secondary mr-4 sub__header" @click="method1">
              Service Merchants
            </h5>
            <h5 class="text-secondary sub__header" @click="method2">
              Product Merchants
            </h5>
          </div>
          <div v-if="this.num == 0" class="mb-5">
            <all-merchants />
          </div>
          <div v-else-if="this.num == 1" class="mb-5">
            <service-merchants />
          </div>
          <div v-else class="mb-5">
            <product-merchants />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AllMerchants from "./AllMerchats";
import ServiceMerchants from "./ServiceMerchants";
import ProductMerchants from "./ProductMerchants";
export default {
  name: "Merchants",
  components: {
    AllMerchants,
    ServiceMerchants,
    ProductMerchants,
  },

  data() {
    return {
      num: 0,
    };
  },
  methods: {
    method() {
      this.num = 0;
    },
    method1() {
      this.num = 1;
    },
    method2() {
      this.num = 2;
    },
  },
};
</script>
