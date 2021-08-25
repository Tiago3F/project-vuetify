<template>
  <div>
    <v-row>
      <v-col md="6">
        <FormsSimpleValidationVcard />
      </v-col>
       <v-col md="6">
        <FormsCustomValidationVcard />
      </v-col>
    </v-row>
  </div>
</template>

<script>
import FormsSimpleValidationVcard from "../components/forms-simple-validations-vcard.vue";
import FormsCustomValidationVcard from "../components/forms-custom-validation-vcard.vue"

export default {
  data() {
    return {};
  },
  components: {
    FormsSimpleValidationVcard,
    FormsCustomValidationVcard
  },
};
</script>

<style scoped>
</style>