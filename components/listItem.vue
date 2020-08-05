<template lang="html">
  <c-list-item>
    <CBox d="flex" bg="#e2e8f0">
      <CBox mr="2" mt="4" ml="4" mb="3" flex="none">
        <c-checkbox
          class="changeMe"
          variant-color="vue"
          bg="#e2e8f0"
          size="lg"
          border-color="vue.500"
          border-width="4px"
          border-radius="sm"
        ></c-checkbox>
      </CBox>

      <CText min-w="75%" font-size="lg" m="1" pt="3" is-truncated>
        {{ listText }}
      </CText>
      <c-icon-button
        variant-color="vue"
        aria-label="Call Jonathan"
        size="sm"
        icon="add"
        mt="3"
      />
      <c-close-button bg="vue.400" color="white" m="3" size="md" />
    </CBox>
    <!--  <listItemEdit /> -->
  </c-list-item>
</template>

<script>
import {
  CBox,
  CListItem,
  CText,
  CCheckbox,
  CIconButton,
  CCloseButton,
} from '@chakra-ui/vue'
// import listItemEdit from '~/components/listItemEdit.vue'
export default {
  name: 'ListItem',
  components: {
    CListItem,
    CText,
    CCheckbox,
    CIconButton,
    CCloseButton,
    CBox,
    //  listItemEdit,
  },
  props: {
    listText: {
      type: String,
      default:
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
    },
  },
}
</script>

<style lang="css">
.css-wcwmhs-class {
  border: none;
  border-radius: 0px;
}
</style>
