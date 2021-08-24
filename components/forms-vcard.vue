<template>
  <div class="form-card">
    <v-row>
      <v-col md="6">
        <v-card height="650px" max-width="750px">
          <v-card-title
            >Inputs <v-spacer></v-spacer>
            <v-btn icon><v-icon>mdi-dots-vertical</v-icon></v-btn>
          </v-card-title>
          <v-card-subtitle
            >A simple text field with placeholder and/or label.</v-card-subtitle
          >
          <v-form>
            <v-container>
              <v-row>
                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Normal field</p>
                </v-col>
                <v-col cols="12" sm="6" md="6">
                  <v-text-field label="Name"></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Label hint</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Input with hint"
                    hint="Some important helper text"
                    persistent-hint
                  ></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Disable input</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field value="Disable" disabled></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Prepend input</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Username"
                    prepend-icon="mdi-account"
                  ></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Password</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Password"
                    prepend-icon="mdi-lock"
                  ></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Appended input</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Append"
                    append-icon="mdi-map-marker"
                  ></v-text-field>
                </v-col>
              </v-row>
            </v-container>
          </v-form>
        </v-card>
      </v-col>

      <v-col md="6">
        <v-card height="650px" max-width="750px">
          <v-card-title
            >Dense <v-spacer></v-spacer>
            <v-btn icon><v-icon>mdi-dots-vertical</v-icon></v-btn>
          </v-card-title>
          <v-card-subtitle
            >You can reduces the text field height with dense prop.
          </v-card-subtitle>
          <v-form>
            <v-container>
              <v-row>
                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Normal field</p>
                </v-col>
                <v-col cols="12" sm="6" md="6">
                  <v-text-field label="Regular"></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Filled field</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Filled"
                    single-line
                    filled
                  ></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Dense & Rounded</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Filled"
                    placeholder="Dense & Rounded"
                    filled
                    rounded
                    dense
                  ></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Prepend input</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Username"
                    prepend-icon="mdi-account"
                  ></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Password</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Password"
                    prepend-icon="mdi-lock"
                  ></v-text-field>
                </v-col>

                <v-col class="mt-5" cols="12" sm="6" md="6">
                  <p>Appended input</p>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-text-field
                    label="Append"
                    append-icon="mdi-map-marker"
                  ></v-text-field>
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
export default {
  data() {
    return {
      show1: false,
      password: "Password",
      rules: {
        required: (value) => !!value || "Required.",
        min: (v) => v.length >= 8 || "Min 8 characters",
      },
    };
  },
};
</script>

<style scoped>
.form-card {
  margin-top: 50px;
}
.inputs {
  margin-top: 70px;
  margin-left: -50px;
}
</style>