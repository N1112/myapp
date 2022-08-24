<template>
  <v-row justify="center">
    <v-dialog v-model="agreementDialog" max-width="1000" persistent>
      <v-card>
        <v-card-title class="headline dialog-title">{{ item.title }}</v-card-title>

        <v-card-text class="dialog-text">
          {{ item.text }}
        </v-card-text>

        <v-card-actions>
          <v-spacer></v-spacer>

          <v-btn color="info" text @click="cancel"> Close </v-btn>
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
        title: '"2016/04/01~2020/03/31" : メディア系大学',
        text: "趣味の音楽を深く学びたいと某大学へ現役入学。\n大学のゼミでは映画や音楽を様々な視点から批評考察することに取り組み、洞察力や観察力を身につける。\n課外活動としてバンドでベースを2年間担当しており、ライブハウスの大人達と共にライブをしコミュニケーション能力を養う。\nまた楽曲制作、レコーディング、CD制作と活動を広げるなかで、ゼロからものづくりをする楽しさやどうすれば曲が良くなるか、どういった楽曲が求められるかを考える発想力を養う。",
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

<style scoped>
  .dialog-title {
    font-size: 1.7em !important;
  }
  .dialog-text {
    font-size: 1.3em !important;
    font-family: Verdana !important;
    white-space: pre-line;
  }
</style>