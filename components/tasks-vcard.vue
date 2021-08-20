<template>
  <div>
    <v-row>
      <v-col>
        <div class="tasks-card">
          <v-card height="733px" max-width="500px">
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
    today: '2019-01-08',
      events: [
        {
          name: 'Weekly Meeting',
          start: '2019-01-07 09:00',
          end: '2019-01-07 10:00',
        },
        {
          name: `Thomas' Birthday`,
          start: '2019-01-10',
        },
        {
          name: 'Mash Potatoes',
          start: '2019-01-09 12:30',
          end: '2019-01-09 15:30',
        },
      ],
  }),
};
</script>


<style scoped>
.tasks-card {
  margin-top: 60px;
}

.calendar-card {
  margin-top: 50px;
  margin-left: -12px;
}
</style>