<template>
  <v-timeline :dense="$vuetify.breakpoint.smAndDown">
    <v-timeline-item color="purple lighten-2" fill-dot right>
      <v-card>
        <v-card-title class="purple lighten-2">
          <v-icon size="42" class="mr-4"> mdi-school-outline  </v-icon>
          <h2 class="text-h4 white--text font-weight-light">
            {{ item1.title }}
          </h2>
        </v-card-title>
        <v-container>
          <v-col cols="12" md="10">
            <p>{{ item1.text }}</p>
          </v-col>
          <agreement-dialog-component
            :agreementDialog="agreementDialog"
            @result="response"
          ></agreement-dialog-component>

          <v-btn  class="ma-2" rounded elevation="13" color="indigo" @click.stop="agreementDialog = true">
            Show More
          </v-btn>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item color="amber lighten-1" fill-dot left>
      <v-card>
        <v-card-title class="amber lighten-1 justify-end">
          <h2 class="text-h4 mr-4 white--text font-weight-light text-right">
            {{ item2.title }}
          </h2>
          <v-icon size="42"> mdi-folder-network-outline </v-icon>
        </v-card-title>
        <v-container>
          <v-col cols="12" md="10">
            <p>{{ item2.text }}</p>
          </v-col>
          <agreement-dialog-component2
            :agreementDialog="agreementDialog2"
            @result="response2"
          ></agreement-dialog-component2>

          <v-btn class="ma-2" rounded elevation="13" color="indigo" @click.stop="agreementDialog2 = true">
            Show More
          </v-btn>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item color="cyan lighten-1" fill-dot right>
      <v-card>
        <v-card-title class="cyan lighten-1">
          <v-icon class="mr-4" size="42"> mdi-api  </v-icon>
          <h2 class="text-h4 white--text font-weight-light">
            {{ item3.title }}
          </h2>
        </v-card-title>
        <v-container>
          <v-col cols="12" md="10">
            <p>{{ item3.text }}</p>
          </v-col>
          <agreement-dialog-component3
            :agreementDialog="agreementDialog3"
            @result="response3"
          ></agreement-dialog-component3>

          <v-btn class="ma-2" rounded elevation="13" color="indigo" @click.stop="agreementDialog3 = true">
            Show More
          </v-btn>
        </v-container>
      </v-card>
    </v-timeline-item>
  </v-timeline>
</template>

<script>
import AgreementDialogComponent from "@/components/atoms/dialog/timelineCardDialog.vue";
import AgreementDialogComponent2 from "@/components/atoms/dialog/timelineCardDialog2.vue";
import AgreementDialogComponent3 from "@/components/atoms/dialog/timelineCardDialog3.vue";
export default {
  name: "TimelineComponent",
  components: {
    "agreement-dialog-component": AgreementDialogComponent,
    "agreement-dialog-component2": AgreementDialogComponent2,
    "agreement-dialog-component3": AgreementDialogComponent3,
  },
  data() {
    return {
      agreementDialog: false,
      agreementDialog2: false,
      agreementDialog3: false,
      item1: {
        title: "\"2016~2020\": 城西国際大学",
        text: "てきすとてきすとてきすとてきすとてきすと",
      },
      item2: {
        title: "\"2020~2021\": 株式会社フォー・クオリア",
        text: "てきすとてきすとてきすとてきすとてきすと2",
      },
      item3: {
        title: "\"2021~\": 株式会社ブリスコラ(常駐)",
        text: "てきすとてきすとてきすとてきすとてきすと3",
      },
      message: "",
    };
  },
  methods: {
    response() {
      this.agreementDialog = false;
    },
    response2() {
      this.agreementDialog2 = false;
    },
    response3() {
      this.agreementDialog3 = false;
    },
  },
};
</script>

<style scoped>
  .text-right {
    text-align: left !important
  }
</style>