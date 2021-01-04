<template lang="">
  <layout>
    <div>
      <Header />
      <Banner />
      <Merchants />
    </div>
  </layout>
</template>

<script>
import Header from "./Header";
import Banner from "./Banner";
import Merchants from "./Merchants";
export default {
  components: {
    Header,
    Banner,
    Merchants,
  },
};
</script>
