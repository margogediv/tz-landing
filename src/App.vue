<template>
  <div id="app">
    <TZHeader/>
    <TZBanner/>
    <TZCouse/>
    <TZServis/>
    <TZGuarantee/>
    <TZReviews/>
    <TZQuestion/>
    <TZCost/>
    <TZForm v-if="closeForm"/>
  </div>
</template>

<script>

import TZHeader from "./components/TZHeader";
import TZBanner from "./components/TZBanner";
import TZCouse from "./components/TZCouse";
import TZServis from "./components/TZServis";
import TZGuarantee from "./components/TZGuarantee";
import TZReviews from "./components/TZReviews";
import TZQuestion from "./components/TZQuestion";
import TZCost from "./components/TZCost";
import TZForm from "./components/TZForm";


export default {
  name: 'App',
  components: {
    TZHeader,
    TZBanner,
    TZCouse,
    TZServis,
    TZGuarantee,
    TZReviews,
    TZQuestion,
    TZCost,
    TZForm
  },

  data() {
    return {
      closeForm: false,
    }
  },
  created() {
    this.$root.$on('changeshowTZForm', () => {
      this.closeForm = false;
    });
    this.$root.$on('showForm', () => {
      this.closeForm = true;
    });
  },
}
</script>

<style lang="scss">
@import 'assets/css/global-css.css';

</style>
