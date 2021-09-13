<template>
  <Layout>
    <div data-v-7f3c42a8="" class="container">
      <div data-v-7f3c42a8="" class="project-header">
        <h1 data-v-7f3c42a8="" class="project-title">{{ $page.list.title }}</h1>
        <div data-v-7f3c42a8="" class="project-info">
          <div data-v-7f3c42a8="" class="categories-container">
            <div data-v-7f3c42a8="" class="categories">
              <span data-v-7f3c42a8="" class="label">Categories</span>
              <span data-v-7f3c42a8="" class="category">{{$page.list.category}}</span>
              <span data-v-7f3c42a8="" class="category">{{$page.list.color}}</span>
            </div>
          </div>
          <div data-v-7f3c42a8="" class="year-container">
            <span data-v-7f3c42a8="" class="label">Year</span>
            <div data-v-7f3c42a8="">{{ $page.list.year }}</div>
          </div>
        </div>
      </div>
      <div data-v-7f3c42a8="" class="content">
        <p>
          {{ $page.list.contact }}
        </p>
        <p>
          <img
            class="g-image g-image--lazy g-image--loaded"
            v-bind:src="
              require('.././assets/pic/' + $page.list.imgname + '.jpg')
            "
            width="2560"
            data-sizes="(max-width: 2560px) 100vw, 2560px"
            sizes="(max-width: 2560px) 100vw, 2560px"
          /><noscript
            ><img
              class="g-image g-image--lazy g-image--loaded"
              v-bind:src="
                require('.././assets/pic/' + $page.list.imgname + '.jpg')
              "
              width="2560"
          /></noscript>
        </p>
      </div>
    </div>
  </Layout>
</template>

<page-query>
  query ($id: ID!) {
  list : strapiList (id : $id) {
    id,
    title,
    categories,
    color,
    contact,
    year,
    imgname
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    title: "project",
  },
};
</script>
