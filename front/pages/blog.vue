<template>
  <div>
    <v-col class="text-center">
      <img src="@/assets/image/blog.png" class="mb-5" />
      <!-- <p>自身が作成した記事の一部</p> -->
    </v-col>
    <div class="v-card-comp" v-for="item in items" :key="item">
      <v-card class="mx-auto" max-width="500" :href="item.link" target="_blank">
        <v-img class="white--text align-end" height="11em" :src="item.src"></v-img>
        <v-card-text>
          <div></div>
          <p class="text-h4 text--primary">
            {{ item.title }}
          </p>
          
        </v-card-text>
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
          title: "GitHubのWebhookによりリポジトリをクローンする",
          link: "https://immediate-fruitadens-3bf.notion.site/BamsCatalog-GitHub-Webhook-4af1137b2ef8411b9aec9a501075591e",
          src: require('@/assets/image/Notion.png')
        },
        blog2: {
          title: "stoplight最新UIのソースを持ってきてアプリUIに取り込む",
          link: "https://immediate-fruitadens-3bf.notion.site/BAMsCatalog-stoplight-UI-d6215d060aab4383a5c8eb778a4f5ede",
          src: require('@/assets/image/Notion.png')
        },
        blog3: {
          title: "画像,PDFファイルのアップロード,ダウンロード機能実装",
          link: "https://immediate-fruitadens-3bf.notion.site/BAMsCatalog-JWA-aaf8196759954afa99bd19d74cddd4f4",
          src: require('@/assets/image/Notion.png')
        },
        blog4: {
          title: "GitLab,GitHubのWebhook連携を行う",
          link: "https://docbase.io/posts/2363286/sharing/095f9146-a335-4345-8553-35f828e4f1b9",
          src: require('@/assets/image/Docbase.png')
        },
        blog5: {
          title: "Stoplight Elementsを試してみる",
          link: "https://docbase.io/posts/2388612/sharing/bfd69dbc-70ce-48d7-a60d-c656d49d86a3",
          src: require('@/assets/image/Docbase.png')
        },
        blog6: {
          title: "OpenAPI Specの基本とStoplight Studioの使い方",
          link: "https://docbase.io/posts/2539970/sharing/b9338129-576c-444d-bec6-932184232993",
          src: require('@/assets/image/Docbase.png')
        },
        blog7: {
          title: "Node.jsにおけるファイル操作モジュール「fs」",
          link: "https://docbase.io/posts/2539976/sharing/bfa73534-4c7e-4f84-8153-218fe1b166ca",
          src: require('@/assets/image/Docbase.png')
        },
      },
    };
  },
};
</script>

<style scoped>
.v-card-comp {
  display: flex;
  justify-content: flex-end;
  margin: 1em 1em 1em 2em;
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

