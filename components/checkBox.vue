<template lang="html">
  <label>
    <c-visually-hidden as="input" type="checkbox" default-checked />

    <c-control-box
      rounded="sm"
      variant-color="vue"
      bg="#e2e8f0"
      size="30px"
      mr="3"
      ml="2"
      border-color="vue.500"
      border-width="2px"
      :_checked="{ bg: 'vue.500', color: 'white', borderColor: 'green.500' }"
      :_focus="{ borderColor: 'vue.500', boxShadow: 'outline' }"
    >
      <c-icon name="check" size="16px" />
    </c-control-box>
  </label>
</template>

<script>
import { CControlBox, CVisuallyHidden, CIcon } from '@chakra-ui/vue'
export default {
  components: {
    CControlBox,
    CVisuallyHidden,
    CIcon,
  },
}
</script>

<style lang="css" scoped></style>
