<template>
  <Layout>
    <div class="container">
      <div class="hero">
        <h1 class="hero-title" _msthash="373179" _msttexthash="25811396">
          CY_Simplicity. Aesthetics. Value.
        </h1>
        <h2 class="hero-subtitle" _msthash="373283" _msttexthash="291249634">
          Hi there, I'm an independent Digital Designer & Art Director focused
          on digital design for brands that like to have fun.
        </h2>
      </div>

      <div data-v-50cbff3e="" class="projects">
        <div
          data-v-50cbff3e=""
          class="project"
          v-for="list in $page.lists.edges"
          :key="list.node.id"
        >
          <g-link
            data-v-50cbff3e=""
            :to="'/post/' + list.node.id"
            class="project-link"
            ><img
              data-v-50cbff3e=""
              :alt="list.node.title"
              v-bind:src="
                require('.././assets/pic/' + list.node.imgname + '.jpg')
              "
              width="2560"
              data-sizes="(max-width: 2560px) 100vw, 2560px"
              class="thumbnail g-image g-image--lazy g-image--loaded"
              _mstalt="7126795"
              sizes="(max-width: 2560px) 100vw, 2560px"
            /><noscript data-v-50cbff3e=""
              ><img
                v-bind:src="
                  require('.././assets/pic/' + list.node.imgname + '.jpg')
                "
                class="thumbnail g-image g-image--loaded"
                width="2560"
                :alt="list.node.title"
            /></noscript>
            <h3
              data-v-50cbff3e=""
              class="project-title"
              _msthash="719255"
              _msttexthash="7126795"
            >
              {{ list.node.title }}
            </h3>
            <div
              data-v-50cbff3e=""
              class="categories"
              _msthash="768577"
              _msttexthash="17596579"
            >
              <span data-v-50cbff3e="" class="category" _istranslated="1">{{
                list.node.categories
              }}</span
              ><span data-v-50cbff3e="" class="category" _istranslated="1">{{
                list.node.color
              }}</span>
            </div>
          </g-link>
        </div>
      </div>
    </div>
    <div data-v-460714ac="">
      <div data-v-460714ac="" class="latest-journals-heading container">
        <span
          data-v-460714ac=""
          class="label"
          _msthash="446187"
          _msttexthash="22651317"
          >Latest and greatest</span
        >
      </div>

      <div data-v-460714ac="" class="latest-journals">
        <div data-v-460714ac="" class="container">
          <g-link
            v-for="article in $page.articles.edges"
            :key="article.node.id"
            data-v-460714ac=""
            :to="'/article/' + article.node.id"
            class="journal"
            ><h3
              data-v-460714ac=""
              class="journal-title"
              _msthash="719125"
              _msttexthash="16304379"
            >
              {{ article.node.title }}
            </h3></g-link
          >
        </div>
      </div>
    </div>
  </Layout>
</template>

<page-query>
  query {
  lists : allStrapiList {
    edges {
      node {
        id
        title
        year
        color
        categories
        imgname
      }
    }
  },
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
    title: "Hello, world!",
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
