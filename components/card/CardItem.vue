<template>
  <div class="card mb-3 mx-5">
    <div class="row g-0">
      <div class="col-md-4">
        <img :src="article.img" class="img-fluid rounded m-2" alt="..." />
      </div>
      <div class="col-md-8">
        <div class="card-body">
          <nuxt-link class="title-task mb-1" :to="'detail/' + article.id">
            <h5 class="card-title">{{ article.title }}</h5>
          </nuxt-link>
          <p class="card-text">
            {{ article.content }}
          </p>
          <p class="card-text">
            <small class="text-muted">Last updated 3 mins ago</small>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    article: {
      type: Object,
      default: "Article",
    },
  },
};
</script>
