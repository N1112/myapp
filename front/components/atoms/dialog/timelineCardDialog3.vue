<template>
  <v-row justify="center">
    <v-dialog v-model="agreementDialog" max-width="1000" persistent>
      <v-card>
        <v-card-title class="headline">{{ item.title }}</v-card-title>

        <v-card-text>
          {{ item.text }}<br>
          <img src="@/assets/image/stoplight.png">
        </v-card-text>

        <v-card-actions>
          <v-spacer></v-spacer>

          <v-btn color="red" text @click="cancel"> Close </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
export default {
  props: {
    agreementDialog: false,
  },
  data() {
    return {
      item: {
        title: "\"2021/08/01~\": 株式会社ブリスコラ(常駐)",
        text: "texttext33333333333",
      },
    };
  },
  methods: {
    cancel() {
      this.$emit("result", { res: true });
    },
  },
};
</script>