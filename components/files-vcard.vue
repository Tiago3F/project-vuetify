<template>
  <div class="files-card">
    <v-card height="290px" max-width="1200px">
      <div>
        <v-row>
            <v-col>
              <v-card-title>Files</v-card-title>
              <v-btn text color="#6c3dff">Work</v-btn>
              <v-btn text color="#6c3dff">Private</v-btn>
              <v-btn text color="#6c3dff">Social</v-btn>
              <v-divider></v-divider>
            </v-col>
          </v-row>
        <div class="align-folders">
          <v-row>
            <v-col md="3">
              <v-img
                class="folders"
                height="120"
                width="160"
                src="https://templates-flatlogic.herokuapp.com/vue-material/img/folder-blue.f2a0a032.svg"
              >
                <div class="folder-title">
                  <p>
                    <strong>UX</strong> <br />
                    178 files
                  </p>
                </div>
              </v-img>
            </v-col>
            <v-col md="3">
              <v-img
                class="folders"
                height="120"
                width="160"
                src="https://templates-flatlogic.herokuapp.com/vue-material/img/folder-pink.ca4eda18.svg"
              >
                <div class="folder-title">
                  <p>
                    <strong>Design</strong> <br />
                    154 files
                  </p>
                </div>
              </v-img>
            </v-col>
            <v-col md="3">
              <v-img
                class="folders"
                height="120"
                width="160"
                src="https://templates-flatlogic.herokuapp.com/vue-material/img/folder-yellow.d553d1c6.svg"
              >
                <div class="folder-title">
                  <p>
                    <strong>Mobile</strong> <br />
                    98 files
                  </p>
                </div>
              </v-img>
            </v-col>
            <v-col md="3">
              <v-img
                class="folders"
                height="120"
                width="160"
                src="https://templates-flatlogic.herokuapp.com/vue-material/img/folder-green.3bc0a33b.svg"
              >
                <div class="folder-title">
                  <p>
                    <strong> Illustration </strong><br />
                    68 files
                  </p>
                </div>
              </v-img>
            </v-col>
          </v-row>
        </div>
      </div>
    </v-card>
  </div>
</template>

<style scoped>
.files-card {
  margin-top: 50px;
}
.folders {
  margin-left: 20px;
  margin-left: 20px;
}

.folder-title {
  margin-top: 70px;
  margin-left: 5px;
  color: #fff;
}
.align-folders {
  margin-left: 50px;
}
</style>