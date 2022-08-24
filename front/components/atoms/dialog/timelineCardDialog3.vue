<template>
  <v-row justify="center">
    <v-dialog v-model="agreementDialog" max-width="1000" persistent>
      <v-card>
        <v-card-title class="headline dialog-title">{{ item.title }}</v-card-title>

        <v-card-text class="dialog-text">
          {{ item.text }}<br>
          <v-spacer></v-spacer>
          <img src="@/assets/image/stoplight.png" class="img-option"><br>
          <span class="stoplight-text">※画像はStoplight Studioのメイン画面。</span>
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
        title: "\"2021/08/01~\" : 株式会社B(常駐)",
        text: "会社のSES事業として他会社へ常駐する。\nAPIに注目しAPIやOpen API Specを扱う様々なアプリケーションを開発している会社で、APIやアプリ開発の技術を吸収していく。\n開発者ポータルとして利用可能なAPIをGit連携し取り込み、リスト表示し提供するというアプリの開発に携わり、Vue.js,Nuxt.jsでフロントエンドを、TypeScriptでバックエンドを開発する。お客様の様々な要件をクリアするべく機能改修を進めていくうちにJavaScriptやそのフレームワークを自身の中で主流言語としていく。\nまた、SwaggerやStoplightを使用しOpen API Specを設計していくことでバックエンドとなるAPIやOpen API Specの知識を高める。",
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
  .img-option {
    margin-top: 1em;
    width: 45em;
  }
  .stoplight-text {
    font-size: 0.8em !important;
    color: white;
  }
</style>