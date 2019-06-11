<template>
  <v-container class="my-2">
    <h1 class="text-xs-center grey--text">
      Skills
    </h1>
    <v-layout row wrap class="my-2">
      <v-flex xs12 sm6 md4 class="pa-2">
        <h2 class="text-xs-center grey--text pa-1">
          プログラミング言語
        </h2>
        <v-expansion-panel ma-3>
          <v-expansion-panel-content
            v-for="(item,i) in items"
            :key="i"
            :class="item.color"
          >
            <template v-slot:header>
              <div>{{ item.title }}</div>
            </template>
            <v-card>
              <v-card-text>{{ item.text }}</v-card-text>
            </v-card>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-flex>
      <v-flex xs12 sm6 md4 class="pa-2">
        <h2 class="text-xs-center grey--text pa-1">
          開発環境・本番環境
        </h2>
        <v-expansion-panel>
          <v-expansion-panel-content
            v-for="(tool,i) in tools"
            :key="i"
            :class="tool.color"
          >
            <template v-slot:header>
              <div>{{ tool.title }}</div>
            </template>
            <v-card>
              <v-card-text>{{ tool.text }}</v-card-text>
            </v-card>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-flex>
      <v-flex xs12 sm6 md4 class="pa-2">
        <h2 class="text-xs-center grey--text pa-1">
          エディタなど
        </h2>
        <v-expansion-panel>
          <v-expansion-panel-content
            v-for="(editor,i) in editors"
            :key="i"
            :class="editor.color"
          >
            <template v-slot:header>
              <div>{{ editor.title }}</div>
            </template>
            <v-card>
              <v-card-text>{{ editor.text }}</v-card-text>
            </v-card>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: 'PHP', color: 'green lighten-1', text: '僕の中の基準となる言語。PHPと比べるとこの言語はこうだなとよく考えます。' },
        { title: 'Laravel', color: 'green lighten-2', text: '便利すぎる部分がある言語。認証の基本的な部分はコマンド一つで終わってしまう。最近一番使ってます。' },
        { title: 'Javascript', color: 'green lighten-4', text: 'なくてはならない言語。このポートフォリオのJSコードの解析にはESLintを使ってます。' },
        { title: 'Vue.js', color: 'green lighten-5', text: 'JavaScriptのフレームワークでは一番触ったことのある言語' },
        { title: 'Nuxt.js', color: 'green lighten-1', text: 'vue-routerとかが置くだけで利用できるのはやはり便利だと感じます。' },
        { title: 'MySQL', color: 'green lighten-2', text: 'SQL言語だと、一番触れたものはこれです。SQL自体はフレームワークのORM使いだしてから、あまり意識できてないです。' },
      ],
      tools: [
        { title: 'VirtualBox', color: 'lime lighten-2', text: 'Laravelの公式開発環境のhomesteadをよく使ってます。vagrantとの組み合わせで使ってます。' },
        { title: 'AWS', color: 'lime lighten-3', text: '無料枠から使い始めました。EC2、S3、Route53、IAM' },
        { title: 'Docker', color: 'lime lighten-1', text: '軽く触った程度です。Dockerfileなどを見よう見まねで、書きましたが利点をあまり実感で来てない状態です。' },
        { title: 'Heroku', color: 'lime lighten-4', text: 'デプロイの環境としてよく使ってました。' },
      ],
      editors: [
        { title: 'VScode', color: 'cyan lighten-1', text: 'エディタはほぼずっとこれです。プラグインとかも簡単に入れられて、一番慣れているエディタです。' },
        { title: 'figma', color: 'cyan lighten-2', text: '無料で画像編集できるので使ってます。もちろん無料なので制限はありますが、ワイヤーフレームのようなこともできるので本当に便利です。' },
        { title: 'draw.io', color: 'cyan lighten-3', text: 'ER図やAWSの構成図を書くのに使ってます。専用の部品が用意されてるのでかなり良いです。' },
      ]
    }
  }
}
</script>
