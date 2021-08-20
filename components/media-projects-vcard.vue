<template>
  <div>
    <v-row>
      <v-col>
        <div class="card-media">
          <v-card class="media-card" max-width="280px">
            <v-card-title>Media </v-card-title>
            <v-container>
              <v-row>
                <v-col>
                  <div class="posts">
                    <v-img
                      class="ml-7"
                      height="40"
                      width="40"
                      src="https://templates-flatlogic.herokuapp.com/vue-material/img/posts.1129c932.svg"
                    >
                    </v-img>
                    <v-card-text class="subtitles">
                      <strong class="values">198</strong><br />
                      <p class="post-information">Posts</p>
                    </v-card-text>
                  </div>

                  <div class="followers">
                    <v-img
                      class="ml-7"
                      height="40"
                      width="40"
                      src="https://templates-flatlogic.herokuapp.com/vue-material/img/followers.bcae40ef.svg"
                    >
                    </v-img>
                    <v-card-text class="subtitles">
                      <strong class="values">12.8K</strong><br />
                      <p class="followers-information">Followers</p>
                    </v-card-text>
                  </div>
                </v-col>
                <v-col md="0">
                  <div class="projects">
                    <v-img
                      class="ml-7"
                      height="40"
                      width="40"
                      src="https://templates-flatlogic.herokuapp.com/vue-material/img/projects.724ba529.svg"
                    >
                    </v-img>
                    <v-card-text class="subtitles">
                      <strong class="values">554 </strong><br />
                      <p class="projects-information">Projects</p>
                    </v-card-text>
                  </div>

                  <div class="following">
                    <v-img
                      class="ml-7"
                      height="40"
                      width="40"
                      src="https://templates-flatlogic.herokuapp.com/vue-material/img/following.b8842c1f.svg"
                    >
                    </v-img>
                    <v-card-text class="subtitles">
                      <strong class="values">1.1k</strong><br />
                      <p class="projects-information">Following</p>
                    </v-card-text>
                  </div>
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </div>
      </v-col>

      <v-col>
        <div class="card-projects">
          <v-card class="projects-card" height="330px" max-width="280px">
            <v-card-title>Projects </v-card-title>
            <v-card-text>
              <div class="font-weight-bold ml-8">Today</div>

              <v-timeline align-top dense>
                <v-timeline-item
                  v-for="projects in project"
                  :key="projects.name"
                  :color="projects.color"
                  small
                >
                  <div>
                    <div class="font-weight-normal">
                      <strong>{{ projects.name }}</strong>
                    </div>
                  </div>
                </v-timeline-item>
              </v-timeline>
            </v-card-text>
          </v-card>
        </div>
      </v-col>
    </v-row>
  </div>
</template>


<script>
export default {
  data: () => ({
    project: [
      {
        name: "Canary",
        color: "#6c3dff",
      },
      {
        name: "Mercury",
        color: "green",
      },
      {
        name: "Yosemite",
        color: "#6c3dff",
      },
       {
        name: "Sputnik",
        color: "#6c3dff",
      },
      
    ],
  }),
};
</script>


<style scoped>
.media-card {
  margin-top: 50px;
}
.items-title {
  margin-top: 10px;
}
.subtitles {
  margin-top: -10px;
  margin-left: 5px;
}
.values {
  margin-left: 10px;
}
.post-information {
  margin-left: 7px;
}

.projects-card {
  margin-top: 50px;
}
</style>