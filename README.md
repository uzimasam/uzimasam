[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com?user=uzimasam&theme=tokyonight&date_format=j%20M%5B%20Y%5D&stroke=DD50B5&fire=DD2727&currStreakNum=2DDD76)](https://git.io/streak-stats)
![Metrics](/github-metrics.svg)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=uzimasam&theme=tokyonight)](https://github.com/anuraghazra/github-readme-stats)
query userInfo($login: String!) {
  user(uzimasam: $login) {
    # fetch only owner repos & not forks
    repositories(ownerAffiliations: OWNER, isFork: false, first: 100) {
      nodes {
        name
        languages(first: 10, orderBy: {field: SIZE, direction: DESC}) {
          edges {
            size
            node {
              color
              name
            }
          }
        }
      }
    }
  }
}
