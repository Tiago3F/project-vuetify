<template>
  <div class="form-card">
    <v-row>
      <v-col >
        <v-card height="350px">
          <v-card-title
            >Selects <v-spacer></v-spacer>
            <v-btn icon><v-icon>mdi-dots-vertical</v-icon></v-btn>
          </v-card-title>
          <v-form>
            <v-container>
              <v-row>
                <v-col cols="12" sm="6" md="6">
                  <v-select :items="['Foo', 'Bar']" label="Standard"></v-select>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-select
                    :items="['Foo', 'Bar']"
                    label="Filled style"
                    filled
                  ></v-select>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-select
                    :items="['Foo', 'Bar']"
                    label="Outlined style"
                    outlined
                  ></v-select>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-select
                    :items="['Foo', 'Bar']"
                    label="Solo field"
                    solo
                  ></v-select>
                </v-col>
              </v-row>
            </v-container>
          </v-form>
        </v-card>
      </v-col>

      <v-col md="6">
        <v-card height="350px">
          <v-card-title
            >Input Variants

            <v-spacer></v-spacer>
            <v-btn icon><v-icon>mdi-dots-vertical</v-icon></v-btn>
          </v-card-title>

          <v-form>
            <v-container>
              <v-row>
                <v-col cols="12" sm="6" md="4">
                  <v-checkbox
                    v-model="colors"
                    label="Primary"
                    color="indigo"
                    value="indigo"
                    hide-details
                  ></v-checkbox>
                </v-col>

                <v-col cols="12" sm="6" md="4">
                  <v-checkbox
                    v-model="colors"
                    label="Secondary"
                    color="pink"
                    value="pink"
                    hide-details
                  ></v-checkbox>
                </v-col>

                <v-col cols="12" sm="6" md="4">
                  <v-checkbox
                    v-model="colors"
                    label="Error"
                    color="orange"
                    value="orange"
                    hide-details
                  ></v-checkbox>
                </v-col>

                <v-col cols="12" sm="6" md="4">
                  <v-radio-group>
                    <v-radio
                      label="Warning"
                      color="orange"
                      value="orange"
                    ></v-radio>
                  </v-radio-group>
                </v-col>

                <v-col cols="12" sm="6" md="4">
                  <v-radio-group>
                    <v-radio
                      label="Success"
                      color="cyan"
                      value="cyan"
                    ></v-radio>
                  </v-radio-group>
                </v-col>

                <v-col cols="12" sm="6" md="4">
                  <v-radio-group>
                    <v-radio
                      label="Info"
                      color="indigo"
                      value="indigo"
                    ></v-radio>
                  </v-radio-group>
                </v-col>

                <v-col cols="12" sm="6" md="11">
                  <v-row align="center">
                    <v-checkbox
                      color="indigo"
                      v-model="enabled"
                      hide-details
                      class="ml-2 mt-0"
                    ></v-checkbox>
                    <v-text-field
                      :disabled="!enabled"
                      label="I only work if you check the box"
                    ></v-text-field>
                  </v-row>
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
      enabled: false,
      colors: ["indigo", "pink", "orange"],
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