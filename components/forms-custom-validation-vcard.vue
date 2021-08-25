<template>
  <div class="custom-validation-card">
    <v-row>
      <v-col md="12">
        <v-card height="500px">
          <v-card-title
            >Custom Validation
            <v-spacer></v-spacer>
            <v-btn icon><v-icon>mdi-dots-vertical</v-icon></v-btn>
          </v-card-title>
          <v-form>
            <v-container>
              <v-row>
                <v-col cols="12" sm="6" md="12">
                  <v-text-field
                    v-model="name"
                    :error-messages="passwordErrors"
                    :counter="8"
                    label="Password"
                    required
                    @input="$v.name.$touch()"
                    @blur="$v.name.$touch()"
                  ></v-text-field>
                </v-col>

                <v-col cols="12" sm="6" md="12"
                  ><v-text-field
                    v-model="phonenumber"
                    :counter="7"
                    :error-messages="phoneNumberErrors"
                    label="Phone Number"
                    required
                    @input="$v.phonenumber.$touch()"
                    @blur="$v.phonenumber.$touch()"
                  ></v-text-field>
                </v-col>

                <v-col cols="12" sm="6" md="12"
                  ><v-text-field
                    v-model="email"
                    :error-messages="emailErrors"
                    label="E-mail"
                    required
                    @input="$v.email.$touch()"
                    @blur="$v.email.$touch()"
                  ></v-text-field>
                </v-col>

                <v-col cols="12" sm="6" md="12">
                  <v-checkbox
                    color="#6c3dff"
                    v-model="checkbox"
                    :error-messages="checkboxErrors"
                    label="I agree to the Terms of Service and Privacy Policy."
                    required
                    @change="$v.checkbox.$touch()"
                    @blur="$v.checkbox.$touch()"
                  ></v-checkbox>
                  <v-divider></v-divider>
                </v-col>

                <v-col class="bottons-validations" cols="12" sm="6" md="12">
                  <v-btn class="mr-4" @click="clear" outlined color="#6c3dff">
                    clear
                  </v-btn>
                  <v-btn class="botton-submit" color="#6c3dff" @click="submit">
                    submit
                  </v-btn>
                </v-col>
              </v-row>
            </v-container>
          </v-form>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import { validationMixin } from "vuelidate";
import { required, minLength, email } from "vuelidate/lib/validators";

export default {
  mixins: [validationMixin],

  validations: {
    name: { required, minLength: minLength(8) },
    phonenumber: { required, minLength: minLength(7) },
    email: { required, email },
    select: { required },
    checkbox: {
      checked(val) {
        return val;
      },
    },
  },

  data: () => ({
    name: "",
    phonenumber: "",
    email: "",
    select: null,
    items: ["Item 1", "Item 2", "Item 3", "Item 4"],
    checkbox: false,
  }),

  computed: {
    passwordErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.minLength &&
        errors.push(
          "Password must contain an upper case letter, a numeric character, and a special character"
        );
      !this.$v.name.required && errors.push("Password is required.");
      return errors;
    },
    phoneNumberErrors() {
      const errors = [];
      if (!this.$v.phonenumber.$dirty) return errors;
      !this.$v.phonenumber.minLength &&
        errors.push("phoneNumber needs to be 7 digits.");
      !this.$v.phonenumber.required && errors.push("PhoneNumber is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Please enter a valid email");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    },
    checkboxErrors() {
      const errors = [];
      if (!this.$v.checkbox.$dirty) return errors;
      !this.$v.checkbox.checked && errors.push("You must agree to continue!");
      return errors;
    },
  },

  methods: {
    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = "";
      this.email = "";
      this.phonenumber = "";
      this.select = null;
      this.checkbox = false;
    },
  },
};
</script>

<style scoped>
.custom-validation-card {
  margin-top: 50px;
}
.bottons-validations {
  margin-left: 570px;
}
.botton-submit {
  color: #fff;
}
</style>