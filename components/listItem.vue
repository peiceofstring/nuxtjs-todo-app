<template lang="html">
  <c-list-item>
    <CFlex bg="#e2e8f0" border-bottom="1px solid black" p="2">
      <listItemEdit :list-text="listText" />
    </CFlex>
  </c-list-item>
</template>

<script>
import { CListItem, CFlex } from '@chakra-ui/vue'
import listItemEdit from '~/components/listItemEdit.vue'

export default {
  name: 'ListItem',
  components: {
    CListItem,
    CFlex,
    listItemEdit,
  },
  props: {
    listText: {
      type: String,
      default:
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ',
    },
  },
}
</script>

<style lang="css"></style>
