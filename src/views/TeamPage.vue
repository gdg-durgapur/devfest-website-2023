<template>
  <v-main class=" pa-0 ma-0">
    <v-container fluid class="my-10">
      <v-row>
        <v-col md="12" sm="12" cols="12" class="text-center google-font">
          <p class="google-font gdg-h1 mb-2 grey--text text--darken-4" style="font-size: 220%">
            Organizers
          </p>
          <p>
              Presenting the Organizers of Devfest 2023
          </p>
        </v-col>

        <v-col md="2" cols="6" sm="3" v-for="(item, index) in coreinfo" :key="index">
          <teamCardVue :item="item" />
        </v-col>
      </v-row>
    </v-container>
    <v-container fluid class="my-10">
      <v-row>
        <v-col md="12" sm="12" cols="12" class="text-center google-font">
          <p class="google-font gdg-h1 mb-2 grey--text text--darken-4" style="font-size: 220%">
            Core Team
          </p>
          <p>
            Presenting the Core Team Members of Devfest 2023
          </p>
        </v-col>

        <v-col md="2" cols="6" sm="3" v-for="(item, index) in teamInfo" :key="index">
          <teamCardVue :item="item" />
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>
  
<script>
import teamJSON from "@/assets/data/team.json";
import coreJSON from "@/assets/data/organizers.json"
import teamCardVue from "@/components/team/teamCard.vue";

export default {
  name: "SpeakersPages",
  components: {
    teamCardVue,
  },
  data: () => ({
      teamInfo: teamJSON,
      coreinfo: coreJSON,
  }),
};
</script>
  
<style></style>