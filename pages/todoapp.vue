<template lang="html">
  <CBox h="100vh" w="100vw" bg="#2b2b2b">
    <listComponent />
  </CBox>
</template>

<script>
import { CBox } from '@chakra-ui/vue'
import listComponent from '~/components/listComponent.vue'
export default {
  components: {
    listComponent,
    CBox,
  },
}
</script>

<style lang="css"></style>
