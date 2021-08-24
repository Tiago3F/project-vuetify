<template>
  <div class="perfil-card">
    <v-card height="290px" max-width="630px">
      <v-row>
        <v-col md="6">
          <v-img
            class="ml-5 mt-6"
            height="200"
            width="200"
            src="https://templates-flatlogic.herokuapp.com/vue-material/img/photo.935dbda0.png"
          ></v-img>
         
        </v-col>

        <v-col md="5">
          <v-card-title>Julee Cruise </v-card-title>
          <v-card-subtitle>
            Product Designer <br />
            <span class="span">Flatlogic.com</span>
          </v-card-subtitle>

          <v-chip-group column>
            <v-chip color="purple" label outlined>UI/UX</v-chip>

            <v-chip color="orange" label outlined>Art</v-chip>

            <v-chip color="pink" label outlined>Design</v-chip>

            <v-chip color="green" label outlined>Illustrator</v-chip>

            <v-chip color="orange" label outlined> Complete </v-chip>
          </v-chip-group>
          <v-btn elevation="0" fab x-small>
            <v-icon>mdi-facebook</v-icon>
          </v-btn>
          <v-btn elevation="0" fab x-small>
            <v-icon>mdi-basketball</v-icon>
          </v-btn>
          <v-btn elevation="0" fab x-small>
            <v-icon>mdi-instagram</v-icon>
          </v-btn>
          <v-btn elevation="0" fab x-small>
            <v-icon>mdi-github</v-icon>
          </v-btn>
          <v-btn elevation="0" fab x-small>
            <v-icon>mdi-twitter</v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-card>
  </div>
</template>

<style scoped>
.perfil-card {
  margin-top: 50px;
}
.span {
  color: #6c3dff;
}

</style>