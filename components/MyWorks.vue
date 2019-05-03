<script>
export default [
  {
    'title': 'RealTimeChat',
    'body': 'Websocketを使ったリアルタイム表示を作ってみたかったので、チャットを作りました。それとソーシャルログインもgithubのみ対応しています。デプロイはHerokuに行なっています。',
    'img': require('assets/images/realtimechat.gif'),
    'img2': require('assets/images/chat.png'),
    'img3': require('assets/images/chat2.png'),
    'url': 'https://laravuechat.herokuapp.com/',
    'github': 'https://github.com/roffet/realchat',
    'tags': ['Laravel', 'Vue.js', 'Pusher'],
  },
  {
    'title': 'hugo-blog',
    'body': 'ブログです。headlessCMSというものを使ってみたくて、Contentfulを使って作りました。フロントの部分はbulma(buefy)を使ってみました。デプロイの部分はnetlifyに助けてもらってます。',
    'img': require('assets/images/blog.png'),
    'img2': require('assets/images/hugoblog.png'),
    'url': 'https://elegant-tesla-c43e26.netlify.com/',
    'github': 'https://github.com/roffet/my-blog',
    'tags': ['Hugo', 'netlify'],
  },
  {
    'title': 'portfolio',
    'body': 'このポートフォリオです。Nuxt.jsを土台にして、VuetifyというUIフレームワークで作りました。デプロイは、GithubPagesにTravisCIを使って行なっています。',
    'img': require('assets/images/portfolio.png'),
    'img2': require('assets/images/portfolio1.png'),
    'img3': require('assets/images/portfolio2.png'),
    'github': 'https://github.com/roffet/my-portfolio',
    'tags': ['Nuxt.js', 'Vuetify', 'TravisCI'],
  },
  {
    'title': 'line bot',
    'body': '製作中です。',
    'img': 'x',
    'img2': require('assets/images/chat2.png'),
    'tags': ['Node.js'],
  },
]
</script>
