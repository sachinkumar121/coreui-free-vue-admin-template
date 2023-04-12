<template>
  <router-view />
</template>
<script>
import { SafeArea } from 'capacitor-plugin-safe-area';

export default {
  mounted() {
    SafeArea.getSafeAreaInsets().then(({ insets }) => {
      // window.alert(JSON.stringify(insets));
    });

    SafeArea.getStatusBarHeight().then(({statusBarHeight}) => {
      // window.alert('statusBarHeight');
      // window.alert(JSON.stringify(statusBarHeight));
    })
  }
}
</script>
<style lang="scss">
// Import Main styles for this application
@import 'styles/style';
</style>
