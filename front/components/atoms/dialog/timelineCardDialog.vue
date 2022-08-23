<template>
  <v-row justify="center">
    <v-dialog v-model="agreementDialog" max-width="1000" persistent>
      <v-card>
        <v-card-title class="headline">{{ item.title }}</v-card-title>

        <v-card-text>
          {{ item.text }}
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
        title: "\"2016/04/01~2020/03/31\": 城西国際大学",
        text: "texttext",
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