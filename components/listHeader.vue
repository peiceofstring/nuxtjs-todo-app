<template lang="html">
  <div class="component-wrapper">
    <CFlex justify-content="center">
      <CBox bg="#2f495e" w="xl" h="3xs" py="16" px="10">
        <CFlex>
          <c-icon name="star" size="32px" color="#00c58e" />
          <CHeading
            mt="1"
            ml="2"
            color="#00c58e"
            as="h2"
            size="lg"
            is-truncated
            >{{ listTitle }}</CHeading
          ></CFlex
        >

        <c-input-group size="lg" mt="5">
          <c-input
            v-model="listInput"
            rounded-right="0"
            placeholder="New To Do Item..."
          />

          <c-button rounded-left="0" bg="#00c58e" color="#2b2b2b" size="lg">
            ADD
          </c-button>
        </c-input-group>
      </CBox>
    </CFlex>
  </div>
</template>

<script>
import {
  CFlex,
  CBox,
  CIcon,
  CHeading,
  CButton,
  CInput,
  CInputGroup,
} from '@chakra-ui/vue'
export default {
  name: 'ListHeader',
  components: {
    CFlex,
    CBox,
    CIcon,
    CHeading,
    CButton,
    CInput,
    CInputGroup,
  },
  props: {
    listTitle: {
      type: String,
      default:
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
    },
    listInput: { type: String, default: '' },
  },
}
</script>

<style lang="css"></style>
