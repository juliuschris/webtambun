<template>
  <Layout>
    <div class="container">
      <div v-for="post in $page.allBlogPost.edges" :key="post.node.id">
        <div v-if="post.node.title!='Profil Desa' && post.node.title!='RS Rujukan'">
          <a :href="post.node.path">
            <div class="card">
              <div class="flex-item">
                <h2>{{ post.node.title}}</h2>
                <p class="sub-text">Diterbitkan {{post.node.date}}</p>
              <!--<g-image src="../assets/logo.png" style="max-width: 50px" class="image"></g-image>-->
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </Layout>
</template>

<script>
export default {};
</script>

<page-query>
query{
  allBlogPost{
    edges{
      node{
          id
        title
        date(format: "MMMM DD, YYYY" )
        path
      }
    }
  }
}
</page-query>

<style scoped>
.sub-text {
  font-size: 14px;
}
.card {
  padding: 5px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: left;
  margin: 12px 100px;
}
.flex-item {
  margin-left: 30px;
}
@media screen and (max-width: 240px) {
  .card {
    margin: 5px;
  }
}
</style>