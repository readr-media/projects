<footer class="footer {$$props.class||''}">
  <h1>相關文章</h1>
  <ul class="footer__article-relatives-list article-relatives-list">
    {#each articleRelatives as article}
      <li class="article-relatives-list__list-item">
        <ArticleRelative
          link={article.link}
          imgSrc={article.imgSrc}
          title={article.title}
          description={article.description}
        />
      </li>
    {/each}
  </ul>
  <div class="footer__credits credits">
    <div>
      <p><span class="bold">記者：</span>尹俞歡</p>
      <p><span class="bold">攝影：</span>潘小俠提供</p>
      <p><span class="bold">專題網頁製作：</span>熊凱文、陳怡蒨、李又如、陳玟諺、簡信昌</p>
    </div>
    <p class="credits__date">2020-08-22</p>
  </div>
</footer>

<script>
  import ArticleRelative from './ArticleRelative.svelte'
  const articleRelatives = [
    {
      link: '',
      imgSrc: '',
      title: '標題標題標題標題標題標題，標題標題標題',
      description: '描述描述描述描述描述描述描述描述描述描述，描述描述描述描述，描述描述描述描述'
    },
    {
      link: '',
      imgSrc: '',
      title: '標題標題標題標題標題標題，標題標題標題',
      description: '描述描述描述描述描述描述描述描述描述描述，描述描述描述描述，描述描述描述描述'
    },
    {
      link: '',
      imgSrc: '',
      title: '標題標題標題標題標題標題，標題標題標題',
      description: '描述描述描述描述描述描述描述描述描述描述，描述描述描述描述，描述描述描述描述'
    }
  ]
</script>

<style lang="scss">
  .footer {
    padding: 50px 20px;
    background-color: #135268;
    &__article-relatives-list {
      margin: 20px 0 0 0;
    }
    &__credits {
      margin: 50px 0 0 0;
    }
  }

  h1 {
    font-size: 20px;
    font-weight: 500;
    letter-spacing: 5px;
    color: #ffffff;
    text-align: center;
    border-top: 2px solid white;
    border-bottom: 2px solid white;
    padding: 10px 0;
  }

  .article-relatives-list {
    &__list-item {
      & + & {
        margin: 38px 0 0 0;
      }
    }
  }

  .credits {
    color: white;
    &__date {
      margin: 20px 0 0 0;
    }
    .bold {
      font-weight: 500;
    }
  }

  @media (min-width: 768px) {
    .footer {
      padding: 50px 0;
      padding-left: calc((100% - 620px) / 2);
      padding-right: calc((100% - 620px) / 2);
    }

    .article-relatives-list {
      display: flex;
      &__list-item {
        & + & {
          margin: 0 0 0 40px;
        }
      }
    }
  }
</style>