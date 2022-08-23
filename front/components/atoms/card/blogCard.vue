<template>
<v-row justify="center">

<!-- ①ボタンは親コンポーネントに移植します
    <v-btn
      color="primary"
      dark
      @click.stop="dialog = true"
    >
      Open Dialog
    </v-btn>
-->
    <!-- ②ダイアログのモデル名はagreementDialogとします -->
    <v-dialog
      v-model="agreementDialog"
      max-width="290"
      persistent
    >
      <v-card>
        <v-card-title class="headline">Use Google's location service?</v-card-title>

        <v-card-text>
          Let Google help apps determine location. This means sending anonymous location data to Google, even when no apps are running.
        </v-card-text>

        <v-card-actions>
          <v-spacer></v-spacer>

          <v-btn
            color="green darken-1"
            text
            @click="agreementDialog = false"
          >
            Disagree
          </v-btn>

          <v-btn
            color="green darken-1"
            text
            @click="agreementDialog = false"
          >
            Agree
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>


<script>
  export default {
    // ③親コンポーネントからのデータはpropsで受け取ることができます。
    props: {
      agreementDialog: false,
    },
  }
</script>