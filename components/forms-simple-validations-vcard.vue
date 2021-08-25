<template>
  <div class="simple-validation-card">
    <v-row>
      <v-col md="12">
        <v-card height="500px">
          <v-card-title
            >Simple Validation

            <v-spacer></v-spacer>
            <v-btn icon><v-icon>mdi-dots-vertical</v-icon></v-btn>
          </v-card-title>
          <v-form ref="form" v-model="valid" lazy-validation>
            <v-container>
              <v-row>
                <v-col class="mt-11" cols="12" sm="6" md="6">
                  <p>Normal field</p>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <v-text-field
                    v-model="name"
                    :counter="10"
                    :rules="nameRules"
                    label="Name"
                    required
                    color="#6c3dff"
                  ></v-text-field>
                </v-col>

                <v-col class="mt-11" cols="12" sm="6" md="6">
                  <p>Email input</p>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <v-text-field
                    v-model="email"
                    :rules="emailRules"
                    label="E-mail"
                    required
                    color="#6c3dff"
                  ></v-text-field>
                </v-col>

                <v-col class="mt-11" cols="12" sm="6" md="6">
                  <p>Simple select</p>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <v-select
                    v-model="select"
                    :items="items"
                    :rules="[(v) => !!v || 'Item is required']"
                    label="Item"
                    required
                    color="#6c3dff"
                  ></v-select>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-checkbox
                    v-model="checkbox"
                    :rules="[(v) => !!v || 'You must agree to continue!']"
                    label="I agree?"
                    required
                  ></v-checkbox>
                </v-col>

                <v-row class="bottons-validations">
                  <v-btn color="#6c3dff" outlined class="mr-4" @click="reset">
                    Reset Form
                  </v-btn>
                  <v-btn
                  color="#6c3dff"
                    class="botton-validate"
                    :disabled="!valid"
                    @click="validate"
                  >
                    Validate
                  </v-btn>
                </v-row>
              </v-row>
            </v-container>
          </v-form>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    name: "",
    nameRules: [
      (v) => !!v || "Name is required",
      (v) => (v && v.length <= 10) || "Name must be less than 10 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+\..+/.test(v) || "E-mail must be valid",
    ],
    select: null,
    items: ["Item 1", "Item 2", "Item 3", "Item 4"],
    checkbox: false,
  }),

  methods: {
    validate() {
      this.$refs.form.validate();
    },
    reset() {
      this.$refs.form.reset();
    },
    resetValidation() {
      this.$refs.form.resetValidation();
    },
  },
};
</script>

<style scoped>
.simple-validation-card {
  margin-top: 50px;
}
.inputs {
  margin-top: 70px;
  margin-left: -50px;
}

.bottons-validations {
  margin-top: 30px;
  margin-left: 120px;
}
.botton-validate {
  color: #fff;
}
</style>