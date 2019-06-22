<template>
  <v-container class="my-2">
    <h1 class="text-xs-center grey--text">
      About me
    </h1>
    <v-timeline align-top class="my-4" :dense="$vuetify.breakpoint.smAndDown">
      <!-- breakpointでdenseを切り替えて表示を変える -->
      <v-timeline-item
        v-for="(item, i) in items"
        :key="i"
        :color="item.color"
        fill-dot
      >
        <v-card
          :color="item.color"
          dark
        >
          <v-card-title class="title">
            {{ item.title }}
          </v-card-title>
          <v-card-text class="white text--primary">
            <p>
              {{ item.text }}
            </p>
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: 'red lighten-2',
        title: '2018年 8月',
        text: 'Progateやドットインストールを始める。最初はHTML、CSS、JavaScriptをやって簡単な少し動きのあるwebサイトを作ったりした。この時はデプロイすることはしていなかった。ちなみに大学時代にも少しだけJavaを触ったことはあったが、その時はプログラミングにのめり込むことはなかった。',
      },
      {
        color: 'cyan lighten-1',
        title: '2018年 11月',
        text: 'このタイミングで2年間勤めた会社を退職して、プログラミングに専念するようになった。この頃にはPHPやRubyなどサーバーサイドの言語を中心に学習していた。開発環境でも形に残るものを作るのは楽しく、だからこそどんなにエラーが出ても続けることができたのだと感じる。'
      },
      {
        color: 'green lighten-1',
        title: '2019年 1月',
        text: 'この頃からconpassというWebサービスを使って、もくもく会に参加するようになる。（最近は時間とお金がばかにならないのであまり参加してない。）またGithubへのコミットで一日の成果を残そうとするようになり、Githubにあるいろんな方のコードを見るようになる。',
      },
      {
        color: 'indigo',
        title: '2019年 3月',
        text: '形に残そうという意識が強くなり、デプロイまでなんとかできるようになってきた。言語一つとっても深く知れば知るほど、まだまだ知らないことばかりだと感じる。',
      }
    ]
  })
}
</script>
