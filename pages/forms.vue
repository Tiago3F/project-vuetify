<template>
  <div>
    <v-row>
      <v-col md="12">
        <FormsInputsDense />
      </v-col>
      <v-col>
        <FormsSelectsInputVariants />
        <FormsTextAreas />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import FormsInputsDense from "../components/forms-inputs-dense-vcard.vue";
import FormsSelectsInputVariants from  "../components/forms-selects-inputvariants.vue"
import FormsTextAreas from "../components/forms-textareas.vue"

export default {
  data() {
    return {};
  },
  components: {
    FormsInputsDense,
    FormsSelectsInputVariants,
    FormsTextAreas
  },
};
</script>

<style scoped>
</style>