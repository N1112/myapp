<template>
<div class="user">
  <v-col class="text-center">
      <img
        src="/v.png"
        alt="Vuetify.js"
        class="mb-5"
      >
      <blockquote class="blockquote">
        作成記事
        <footer>
            <a href="https://immediate-fruitadens-3bf.notion.site/BamsCatalog-GitHub-Webhook-4af1137b2ef8411b9aec9a501075591e" target="_blank">BamsCatalog改修:GitHubのWebhookにも対応させる</a><br>
            <a href="https://immediate-fruitadens-3bf.notion.site/BAMsCatalog-stoplight-UI-d6215d060aab4383a5c8eb778a4f5ede" target="_blank">BAMsCatalog改修:stoplight最新UIのソースを持ってきてカタログに取り込む</a><br>
            <a href="https://immediate-fruitadens-3bf.notion.site/BAMsCatalog-JWA-aaf8196759954afa99bd19d74cddd4f4" target="_blank">BAMsCatalog改修:JWA向け改修→添付資料のアップロード機能</a><br>
            <a href="https://docbase.io/posts/2363286/sharing/095f9146-a335-4345-8553-35f828e4f1b9" target="_blank">各GitのWebhook連携を行う、GitLabとGitHubのnpmライブラリを使用して必要なプロジェクト情報を取得する</a><br>
            <a href="https://docbase.io/posts/2388612/sharing/bfd69dbc-70ce-48d7-a60d-c656d49d86a3" target="_blank">Stoplight Elementsを試してみる</a><br>
            <a href="https://docbase.io/posts/2539970/sharing/b9338129-576c-444d-bec6-932184232993" target="_blank">OpenAPI Specの基本とStoplight Studioの使い方</a><br>
            <a href="https://docbase.io/posts/2539976/sharing/bfa73534-4c7e-4f84-8153-218fe1b166ca" target="_blank">Node.jsにおけるファイル操作モジュール「fs」</a><br>
        </footer>
      </blockquote>
    </v-col>

  <div class="v-card">
    <v-card
      class="mx-auto"
      max-width="344"
    >
      <v-card-text>
        <div>Word of the Day</div>
        <p class="text-h4 text--primary">
          be•nev•o•lent
        </p>
        <p>adjective</p>
        <div class="text--primary">
          well meaning and kindly.<br>
          "a benevolent smile"
        </div>
      </v-card-text>
      <v-card-actions>
        <v-btn
          text
          color="deep-purple accent-4"
        >
          Learn More
        </v-btn>
      </v-card-actions>
    </v-card>




    <v-card
      class="mx-auto"
      max-width="344"
    >
      <v-card-text>
        <div>Word of the Day</div>
        <p class="text-h4 text--primary">
          be•nev•o•lent
        </p>
        <p>adjective</p>
        <div class="text--primary">
          well meaning and kindly.<br>
          "a benevolent smile"
        </div>
      </v-card-text>
      <v-card-actions>
        <v-btn
          text
          color="deep-purple accent-4"
        >
          Learn More
        </v-btn>
      </v-card-actions>
    </v-card>
  </div>

</div>
</template>

<script>
export default {
  name: 'InspirePage'
}
</script>

<style scoped>
  .v-card {
    display: flex;
    justify-content: flex-end;
  }
  .form-btn {
    display: flex;
    justify-content: flex-end;
  }
  .date-picker {
    padding: 0.6em 0 2em 0;
  }
</style>

