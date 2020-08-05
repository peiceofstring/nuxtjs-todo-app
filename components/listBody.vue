<template lang="html">
  <div class="component-wrapper">
    <CBox d="flex" justify-content="center">
      <CBox w="xl">
        <c-list>
          <listItem />
          <listItem
            v-for="item in ['First Item', 'Second Item', 'Third Item']"
            :key="item"
            :list-text="item"
          />

          /></c-list
        >
      </CBox>
    </CBox>
  </div>
</template>

<script>
import { CBox, CList } from '@chakra-ui/vue'
import listItem from '~/components/listItem.vue'
export default {
  name: 'ListBody',
  components: {
    CBox,
    CList,
    listItem,
  },
}
</script>

<style lang="css"></style>
