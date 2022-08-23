<template>
  <div class="user">
    <v-col class="text-center">
      <img src="/v.png" alt="Vuetify.js" class="mb-5" />
      <p>自身が作成した記事の一部</p>
    </v-col>

    <div class="v-card" v-for="item in items" :key="item">
      <v-card class="mx-auto" max-width="500">
        <v-card-text>
          <div></div>
          <p class="text-h4 text--primary">
            {{ item.title }}
          </p>
          
        </v-card-text>
        <v-card-actions>
          <a :href="item.link" target="_blank"
            ><v-btn class="mx-2" fab dark large color="purple">
              <v-icon dark> mdi-post-outline </v-icon>
            </v-btn></a
          ><br />
        </v-card-actions>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlogPage",
  data() {
    return {
      items: {
        blog: {
          title: "BamsCatalog改修:GitHubのWebhookにも対応させる",
          link: "https://immediate-fruitadens-3bf.notion.site/BamsCatalog-GitHub-Webhook-4af1137b2ef8411b9aec9a501075591e",
        },
        blog2: {
          title:
            "BAMsCatalog改修:stoplight最新UIのソースを持ってきてカタログに取り込む",
          link: "https://immediate-fruitadens-3bf.notion.site/BAMsCatalog-stoplight-UI-d6215d060aab4383a5c8eb778a4f5ede",
        },
        blog3: {
          title: "BAMsCatalog改修:JWA向け改修→添付資料のアップロード機能",
          link: "https://immediate-fruitadens-3bf.notion.site/BAMsCatalog-JWA-aaf8196759954afa99bd19d74cddd4f4",
        },
        blog4: {
          title:
            "各GitのWebhook連携を行う、GitLabとGitHubのnpmライブラリを使用して必要なプロジェクト情報を取得する",
          link: "https://docbase.io/posts/2363286/sharing/095f9146-a335-4345-8553-35f828e4f1b9",
        },
        blog5: {
          title: "Stoplight Elementsを試してみる",
          link: "https://docbase.io/posts/2388612/sharing/bfd69dbc-70ce-48d7-a60d-c656d49d86a3",
        },
        blog6: {
          title: "OpenAPI Specの基本とStoplight Studioの使い方",
          link: "https://docbase.io/posts/2539970/sharing/b9338129-576c-444d-bec6-932184232993",
        },
        blog7: {
          title: "Node.jsにおけるファイル操作モジュール「fs」",
          link: "https://docbase.io/posts/2539976/sharing/bfa73534-4c7e-4f84-8153-218fe1b166ca",
        },
      },
    };
  },
};
</script>

<style scoped>
.v-card {
  display: flex;
  justify-content: flex-end;
  /* margin-bottom: 55px; */
  margin: 15px 15px 15px 30px;
  /* padding-bottom: 30px; */
  float: left;
  align-items: center;
}
.form-btn {
  display: flex;
  justify-content: flex-end;
}
.date-picker {
  padding: 0.6em 0 2em 0;
}
</style>

