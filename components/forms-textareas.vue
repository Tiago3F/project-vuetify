<template>
  <div class="form-card">
    <v-row>
      <v-col md="12">
        <v-card>
          <v-card-title
            >Selects <v-spacer></v-spacer>
            <v-btn icon><v-icon>mdi-dots-vertical</v-icon></v-btn>
          </v-card-title>
          <v-form>
            <v-container>
              <v-row>
                <v-col cols="12" sm="6" md="6">
                  <v-textarea
                    color="#6c3dff"
                    label="Default style"
                    value="Alice was beginning to get very tired of sitting by her sister on the bank, and of having nothing to do: once or twice she had peeped into the book her sister was reading, but it had no pictures or conversations in it, “and what is the use of a book,” thought Alice “without pictures or conversations?"
                  ></v-textarea>
                </v-col>

                <v-col cols="12" sm="6" md="6"
                  ><v-textarea
                    solo
                    value="“What a curious feeling!” said Alice; “I must be shutting up like a telescope.”"
                    label="Solo textarea"
                  ></v-textarea>
                </v-col>

                <v-col cols="12" sm="6" md="6"
                  ><v-textarea
                    color="#6c3dff"
                    filled
                    label="Filled textarea"
                    value="And so it was indeed: she was now only ten inches high, and her face brightened up at the thought that she was now the right size for going through the little door into that lovely garden. First, however, she waited for a few minutes to see if she was going to shrink any further: she felt a little nervous about this; “for it might end, you know,” said Alice to herself, “in my going out altogether, like a candle. I wonder what I should be like then?”"
                  ></v-textarea>
                </v-col>

                <v-col cols="12" sm="6" md="6">
                  <v-textarea
                    color="#6c3dff"
                    outlined
                    label="Outlined textarea"
                    value="Soon her eye fell on a little glass box that was lying under the table: she opened it, and found in it a very small cake, on which the words “EAT ME” were beautifully marked in currants. “Well, I’ll eat it,” said Alice, “and if it makes me grow larger, I can reach the key; and if it makes me grow smaller, I can creep under the door; so either way I’ll get into the garden, and I don’t care which happens!”"
                  ></v-textarea>
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