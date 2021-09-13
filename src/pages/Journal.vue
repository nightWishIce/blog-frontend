<template>
  <Layout>
    <div data-v-da896d1e="" class="container">
      <div data-v-da896d1e="" class="journal-hero">
        <h1 data-v-da896d1e="" class="journal-header">
          a wise person once said...
        </h1>
      </div>
    </div>
    <g-link v-for="article in $page.articles.edges" :key="article.node.id"
      data-v-da896d1e=""
      :to="'/article/' + article.node.id"
      class="journal-post"
      ><div data-v-da896d1e="" class="container journal">
        <h2 data-v-da896d1e="" class="journal-title">
          {{article.node.title}}
        </h2>
        <p data-v-da896d1e="" class="journal-excerpt">
          {{article.node.subtitle}}
        </p>
      </div>
      </g-link>
  </Layout>
</template>

<page-query>
query {
  articles : allStrapiArticle {
    edges {
      node {
        id
        title
        subtitle
        author
        date
        content
      }
    }
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    title: "Journal",
  }
};
</script>
