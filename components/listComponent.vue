<template lang="html">
  <div class="component-wrapper">
    <listHeader />
    <listBody />
  </div>
</template>

<script>
import listHeader from '~/components/listHeader.vue'
import listBody from '~/components/listBody.vue'
export default {
  name: 'ListComponent',
  components: {
    listHeader,
    listBody,
  },
}
</script>

<style lang="css"></style>
