<template>
  <v-container fluid class="pa-0">
    <v-row align="center" class>
      <v-col cols="12" md="12" lg="12" sm="12" class="pa-0" style="color:white">
        <div class="ma-1">
          <div class="pa-5">
            <p class="google-font mb-0" style="font-size:150%">About Developer Student Clubs PDPU</p>
            <p
              class="google-font mt-0"
              style="font-size:95%"
            >A Developer Students Club is a Google recognized student body at a college which directly reports to Google for their activities and is supported by the tech giant. A DSC conducts workshops, seminars and other fun activities which help the students connect with Google.</p>
            <!-- <v-btn
              v-if="checkExistance(config.generalConfig.meetupLink,0)"
              :href="config.generalConfig.meetupLink"
              target="_blank"
              outlined
              color
              class="ma-0 google-font mb-2"
              style="border-radius:5px;text-transform: capitalize;color:white"
            >Meetup Page</v-btn>&nbsp; -->  <!-- the meetup button -->
            <br />
            <router-link
              to="/about"
              class="google-font"
              style="text-decoration:none;color:white"
            >See More about DSC PDPU</router-link>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "App",
  data: () => ({}),
  computed: {
    ...mapState(["config"])
  }
};
</script>