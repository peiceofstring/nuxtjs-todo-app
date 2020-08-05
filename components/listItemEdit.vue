<template>
  <c-editable default-value="Take some chakra ⚡️ (click me)" font-size="2xl">
    <template v-slot="{ isEditing, onSubmit, onCancel, onRequestEdit }">
      <c-editable-preview />
      <c-editable-input />
      <c-flex mt="3">
        <c-button-group v-if="isEditing" size="sm">
          <c-icon-button icon="check" color="green" @click="onSubmit" />
          <c-icon-button icon="close" @click="onCancel" />
        </c-button-group>
        <c-icon-button v-else icon="edit" size="sm" @click="onRequestEdit" />
      </c-flex>
    </template>
  </c-editable>
</template>

<script>
import { CEditable, CEditableInput, CEditablePreview } from '@chakra-ui/vue'

export default {
  name: 'ListItemEdit',
  components: {
    CEditable,
    CEditableInput,
    CEditablePreview,
  },
}
</script>

<style lang="css"></style>
