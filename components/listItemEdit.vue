<template>
  <c-editable :value="listText" font-size="lg">
    <template v-slot="{ isEditing, onSubmit, onCancel, onRequestEdit }">
      <c-flex>
        <c-box> <checkBox /></c-box>
        <c-box>
          <c-editable-preview w="26rem" />
          <c-editable-input size="lg" />
        </c-box>
        <c-box>
          <c-button-group v-if="isEditing" size="sm" d="flex" ml="6">
            <c-icon-button
              aria-label="Close Editor"
              variant-color="vue"
              icon="close"
              @click="onCancel"
            />
            <c-icon-button
              aria-label="Submit Edit"
              variant-color="vue"
              icon="check"
              color="vue"
              @click="onSubmit"
            />
          </c-button-group>

          <c-button-group v-else ml="6" d="flex">
            <c-icon-button
              aria-label="Edit Item"
              variant-color="vue"
              size="sm"
              icon="add"
              @click="onRequestEdit"
            />
            <c-icon-button
              aria-label="Remove Item"
              variant-color="vue"
              size="sm"
              icon="close"
            />
          </c-button-group>
        </c-box>
      </c-flex>
      <c-grid> </c-grid>
    </template>
  </c-editable>
</template>

<script>
import {
  CEditable,
  CEditableInput,
  CEditablePreview,
  CFlex,
  CButtonGroup,
  CIconButton,
  // CGrid,
} from '@chakra-ui/vue'
import checkBox from '~/components/checkBox.vue'
export default {
  name: 'ListItemEdit',
  components: {
    CEditable,
    CEditableInput,
    CEditablePreview,
    CFlex,
    CButtonGroup,
    CIconButton,
    checkBox,
    //  CGrid,
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
