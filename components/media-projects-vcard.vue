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
            <v-progress-circular
              class="circular"
              :rotate="180"
              :size="100"
              :width="15"
              :value="value"
              color="rgb(255, 92, 147)"
              background-color="green lighten-1"
            >
              {{ value }}%
            </v-progress-circular>
            <v-card-text class="informations">
              <span class="new"></span>New
              <span class="progress"></span>Progress
              <span class="completed"></span>Completed <br />
              <span class="canceled"></span>Canceled
            </v-card-text>
            <v-btn class="botton-detail" outlined color="#6c3dff">
              Detail
            </v-btn>
          </v-card>
        </div>
      </v-col>
    </v-row>
  </div>
</template>


<script>
export default {
  data() {
    return {
      value: 70,
    };
  },
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
.circular {
  margin-top: 20px;
  margin-left: 90px;
}
.informations {
  margin-left: 20px;
}
.new {
  background: rgb(83, 109, 254);
  color: rgb(83, 109, 254);
  height: 8px;
  width: 8px;
  left: 0px;
  top: 0px;
  border-width: 0px;
  border-color: rgb(255, 255, 255);
  border-radius: 12px;
  position: relative;
  display: inline-block;
  cursor: pointer;
  margin-right: 3px;
  border-style: solid;
}
.progress {
  background: rgb(255, 92, 147);
  color: rgb(255, 92, 147);
  height: 8px;
  width: 8px;
  left: 0px;
  top: 0px;
  border-width: 0px;
  border-color: rgb(255, 255, 255);
  border-radius: 12px;
  position: relative;
  display: inline-block;
  cursor: pointer;
  margin-right: 3px;
  border-style: solid;
}
.completed {
  background: rgb(60, 212, 160);
  color: rgb(60, 212, 160);
  height: 8px;
  width: 8px;
  left: 0px;
  top: 0px;
  border-width: 0px;
  border-color: rgb(255, 255, 255);
  border-radius: 12px;
  position: relative;
  display: inline-block;
  cursor: pointer;
  margin-right: 3px;
  border-style: solid;
}
.canceled {
  background: rgb(255, 194, 96);
  color: rgb(255, 194, 96);
  height: 8px;
  width: 8px;
  left: 0px;
  top: 0px;
  border-width: 0px;
  border-color: rgb(255, 255, 255);
  border-radius: 12px;
  position: relative;
  display: inline-block;
  cursor: pointer;
  margin-right: 3px;
  border-style: solid;
}
.botton-detail {
  float: right;
  margin-right: 20px;
}
</style>