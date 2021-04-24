<template>
  <div class="timeline">
    <v-container>
      <v-timeline>
        <v-timeline-item
          v-for="(year, i) in years"
          :key="i"
          :color="year.color"
          :achievement="year.achievement"
          small
        >
          <template v-slot:opposite>
            <span
              :class="`headline font-weight-bold ${year.color}--text`"
              v-text="year.year"
            ></span>
          </template>
          <div class="py-4">
            <h2 :class="`headline font-weight-bold mb-4 ${year.color}--text`">
              {{ year.achievement }}
            </h2>
            <div>
              <!-- <h2>checking</h2> -->
            </div>
          </div>
        </v-timeline-item>
      </v-timeline>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    years: [
      {
        color: "cyan",
        year: "1999",
        achievement: "Born 😅",
      },
      {
        color: "green",
        year: "2014",
        achievement: "Completed High School 🏫",
      },
      {
        color: "pink",
        year: "2016",
        achievement: "Completed Intermediate 🏫",
      },
      {
        color: "amber",
        year: "2020",
        achievement: "Completed Graduation 🎓",
      },
      {
        color: "orange",
        year: "2021",
        achievement: "Started Job @HCL 🏢",
      },
    ],
  }),
};
</script>

<style scoped>
</style>