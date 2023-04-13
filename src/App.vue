<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppCta from './components/AppCta.vue';

export default {
    components: { 
      AppHeader,
      AppMain,
      AppCta,
    },
    data () {
      return {

      }
    }
}
</script>

<template>
  <AppHeader />
  <AppMain/>
  <AppCta/>
</template>

<style lang="scss">
@use "./style/general.scss" as *;
</style>
