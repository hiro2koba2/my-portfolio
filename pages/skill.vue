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
          開発環境
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
        { title: 'PHP', color: 'green lighten-1', text: '' },
        { title: 'Laravel', color: 'green lighten-2', text: '便利すぎる部分がある言語、認証の基本的な部分はコマンド一つで終わってしまう。もちろん通常の認証以外もつけるとは思いますが。' },
        { title: 'Javascript', color: 'green lighten-4', text: 'このポートフォリオのコードの解析にはESLintを使ってます。' },
        { title: 'Vue.js', color: 'green lighten-5', text: 'About' },
        { title: 'Nuxt.js', color: 'green lighten-1', text: 'vue-routerとかが置くだけで利用できるのはやはり便利だと感じます。' },
        { title: 'MySQL', color: 'green lighten-2', text: 'SQL言語だと、一番触れたものはこれです。ログインしてSQL直書きでDBやテーブルの中身見たりしてました。今はテーブルプラスっていうアプリケーションで確認することの方が多いです。'},
      ],
      tools: [
        { title: 'VirtualBox', color: 'lime lighten-2', text: 'Laravelの公式開発環境のhomesteadをよく使ってます。' },
        { title: 'AWS', color: 'lime lighten-3', text: '使い始めました、今一番勉強してるところでもあります。この分野を知ることで、今までわからなかったことが繋がってきた感覚があります。EC2、S3、Cloudfront、Route53、IAM、Codedeploy、etc' },
        { title: 'Docker', color: 'lime lighten-1', text: '軽く触った程度です。Dockerfileなども見よう見まねで、書きましたが利点をあまり実感で来てない状態です。' },
        { title: 'Heroku', color: 'lime lighten-4', text: 'デプロイの環境として一番使わせてもらいました。' },
      ],
      editors: [
        { title: 'VScode', color: 'cyan lighten-1', text: 'エディタはほぼずっとこれです。プラグインとかも簡単に入れられて、一番慣れているエディタです。' },
        { title: 'figma', color: 'cyan lighten-2', text: '無料で画像編集できるので使ってます。もちろん無料なので制限はありますが、ワイヤーフレームのようなこともできるので本当に便利です。' },
        { title: 'draw.io', color: 'cyan lighten-3', text: 'ER図やAWSの構成図を書くのに使ってます。専用の部品が用意されてるのでかなり良いです。'},
      ]
    }
  }
}
</script>
