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
        title: "\"2020/04/01~2021/07/31\" : 株式会社F",
        text: "未経験エンジニアとして新卒入社。\nPHP外部研修を行い社会人マナー研修とHTML,CSS,PHP,MySQLを使用した掲示板の作成をグループで行う。\nその後1年程単体テスト、結合テストを中心に案件に携わりながらコーディングの勉強を進める。\n2021年から本格的に開発案件にアサインされ、半年ほどLaravelを使用した案件にてフロントエンド、バックエンドの各機能を開発。\nその後の案件ではDB設計、Swaggerを使用したAPI設計を担当する。\n様々な案件を通しフロントエンドとしてWebサイトの画面を作成することの楽しさや達成感を覚える。",
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