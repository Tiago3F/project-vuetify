<template>
  <div>
    <v-row>
      <v-col>
        <div class="tasks-card">
          <v-card height="725px" max-width="500px">
            <div>
              <v-row>
                <v-col>
                  <v-card-title>Tasks</v-card-title>
                  <v-btn text color="#6c3dff">Today</v-btn>
                  <v-btn text color="#6c3dff">This Week</v-btn>
                  <v-btn text color="#6c3dff">This Month</v-btn>
                  <v-divider></v-divider>
                  <v-card-text>
                    <div class="font-weight-bold ml-11">Today</div>

                    <v-card-text class="py-0">
                      <v-timeline align-top dense>
                        <v-timeline-item color="#ffc86f" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>10:21</strong>
                            </v-col>
                            <v-col>
                              <strong>Call conference with a New Client</strong>
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#a6b3ff" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>11:30</strong>
                            </v-col>
                            <v-col>
                              <strong
                                >Presentation Demo Ecological Project</strong
                              >
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#ffc86f" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>12:30</strong>
                            </v-col>
                            <v-col>
                              <strong>Call with PR Manager</strong>
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#68deb6" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>14:00</strong>
                            </v-col>
                            <v-col>
                              <strong>Interview with a new UI/UX</strong>
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#ff5992" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>15:00</strong>
                            </v-col>
                            <v-col>
                              <strong>Call conference with a New Client</strong>
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#ffc86f" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>15:45</strong>
                            </v-col>
                            <v-col>
                              <strong
                                >Presentation Demo Ecological Project</strong
                              >
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#68deb6" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>16:00</strong>
                            </v-col>
                            <v-col>
                              <strong>Interview with a new UI/UX</strong>
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#ffc86f" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>17:00</strong>
                            </v-col>
                            <v-col>
                              <strong>Call conference with a New Client</strong>
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#a6b3ff" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>17:25</strong>
                            </v-col>
                            <v-col>
                              <strong
                                >Presentation Demo Ecological Project</strong
                              >
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#ff5992" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>17:40</strong>
                            </v-col>
                            <v-col>
                              <strong>Interview with a new UI/UX</strong>
                            </v-col>
                          </v-row>
                        </v-timeline-item>

                        <v-timeline-item color="#a6b3ff" small>
                          <v-row class="pt-1">
                            <v-col cols="2">
                              <strong>18:00</strong>
                            </v-col>
                            <v-col>
                              <strong
                                >Presentation Demo Ecological Project</strong
                              >
                            </v-col>
                          </v-row>
                        </v-timeline-item>
                      </v-timeline>
                    </v-card-text>
                  </v-card-text>
                </v-col>
              </v-row>
            </div>
          </v-card>
        </div>
      </v-col>

      <v-col md="5">
        <div class="card-projects">
          <v-card class="calendar-card" height="330px" max-width="500px">
            <v-date-picker
              class="calendar"
              color="#6c3dff"
              width="340px"
              no-title
              v-model="date2"
              :event-color="(date) => (date[9] % 2 ? '#ffc86f' : '#68deb6')"
              :events="functionEvents"
            ></v-date-picker>
          </v-card>
        </div>

        <div class="viwers-card">
          <v-card class="views-card" height="200px" max-width="500px">
            <v-card-title
              >Views <v-spacer></v-spacer> <v-icon>mdi-dots-vertical</v-icon>
            </v-card-title>
            <v-card-subtitle class="mt-2">
              <h2>7,156</h2>
              <span class="span">7.2%</span>
              <v-sparkline
                class="sparkline"
                :value="value"
                color="#ffb2de"
                fill
                :smooth="radius"
              ></v-sparkline>

              <v-btn class="botton-see-more" outlined color="#6c3dff" x-small>
                See More
              </v-btn>
            </v-card-subtitle>
          </v-card>
        </div>

        <div class="update-card">
          <v-card
            class="views-card"
            height="95px"
            max-width="500px"
            color="#6c3dff"
          >
            <v-card-title>
              <img
                src="https://templates-flatlogic.herokuapp.com/vue-material/img/update-icon.88cea971.svg"
              />
              <p class="views">Updates</p>
              <v-spacer></v-spacer>
              <v-btn class="ma-2 mt-3" outlined color="#fff"> Detail </v-btn>
            </v-card-title>
          </v-card>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    radius: 20,
    arrayEvents: null,
    date1: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
      .toISOString()
      .substr(0, 10),
    date2: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
      .toISOString()
      .substr(0, 10),
    value: [423, 446, 800, 510, 1000, 610, 760],
  }),
  methods: {
    functionEvents(date) {
      const [, , day] = date.split("-");
      if ([12, 17, 28].includes(parseInt(day, 10))) return true;
      if ([1, 19, 22].includes(parseInt(day, 10)))
        return ["#ff5992", "#ffc86f"];
      return false;
    },
  },
};
</script>


<style scoped>
.tasks-card {
  margin-top: 60px;
}
.span {
  color: #3cd4a0;
  font-size: 12px;
}
.calendar-card {
  margin-top: 50px;
  margin-left: -12px;
}
.views-card {
  margin-top: 50px;
  margin-left: -12px;
}
.calendar {
  margin-left: 25px;
  margin-top: 25px;
}
.sparkline {
  padding-left: 50px;
  margin-top: -25px;
  margin-left: 30px;
  width: 330px;
}
.botton-see-more {
  margin-top: -50px;
}
.views {
  color: #fff;
  margin-top: 15px;
  margin-left: 10px;
}
</style>