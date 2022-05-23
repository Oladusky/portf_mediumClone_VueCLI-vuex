<template>
  <div>
    <mcv-topbar />

    <router-view></router-view>
  </div>
</template>

<style></style>



<script> 

import McvTopbar from '@/components/Topbar'
import { actionTypes } from './store/modules/auth'
export default {
  name: 'McvApp',
  components: {
    McvTopbar
  },
  mounted() {
    console.log('hi')
    this.$store.dispatch(actionTypes.getCurrentUser)
  }
}
</script>
