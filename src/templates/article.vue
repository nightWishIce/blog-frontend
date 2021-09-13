<template>
  <Layout>
    <div data-v-2a0eef53="" class="journal">
      <div data-v-2a0eef53="" class="container journal-container">
        <div data-v-2a0eef53="" class="journal-header">
          <h1 data-v-2a0eef53="" class="journal-title">
            {{$page.article.title}}
          </h1>
          <img v-bind:src="require('.././assets/pic/' + $page.article.id + '.jpg')">
          
          <div data-v-2a0eef53="" class="journal-meta">
            <div data-v-2a0eef53="" class="journal-author">
              <span data-v-2a0eef53="" class="label">Author</span
              ><span data-v-2a0eef53="" class="author-name"
                >{{$page.article.author}}</span
              >
            </div>
            <div data-v-2a0eef53="" class="journal-date">
              <span data-v-2a0eef53="" class="label">Date</span>
              <div data-v-2a0eef53="">7. June 2019 : {{$page.article.date}}</div>
            </div>
            <div data-v-2a0eef53="" class="journal-time">
              <span data-v-2a0eef53="" class="label">Time</span
              ><span data-v-2a0eef53="">1 min read</span>
            </div>
          </div>
        </div>
        <div data-v-2a0eef53="" class="journal-content"
          v-html="mdToHtml($page.article.content)"
        >
        </div>
      </div>
    </div>
  
  </Layout>
</template>

<page-query>
  query ($id: ID!) {
  article : strapiArticle (id : $id) {
    id
    title
    subtitle
    author
    date
    content
  }
}
</page-query>

<script>
import MarkdownIt from 'markdown-it'
const md = new MarkdownIt()
export default {
  metaInfo: {
    title: "article",
  },
  methods : {
    mdToHtml (markdown) {
      return md.render(markdown)
    }
  }
};
</script>
