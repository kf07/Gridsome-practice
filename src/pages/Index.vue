<template>
    <Layout>
        <h1 class="mainTitle">Blog Posts</h1>
        <div class="test">
            <a href=""></a>
        </div>
        <div v-for="item in $page.allBlogPost.edges" :key="item.path" class="post">
            <h2>
                <g-link :to="item.node.path">{{ item.node.title }}</g-link>
            </h2>
            <dl>
                <dt>{{ item.node.date }}</dt><dd>{{ item.node.fields.tags}}</dd>
            </dl>
            <p>{{ item.node.fields.description }}</p>
            <g-link :to="item.node.path" class="continue-link">続きを読む ></g-link>
        </div>
    </Layout>
</template>

<page-query>
    query Home ($page: Int) {
    allBlogPost (page: $page) {
    edges {
    node {
    _id
    title
    date (format: "YYYY年MM月DD日 HH:mm:ss")
    fields {
    description
    tags
    }
    path
    }
    }
    }
    }
</page-query>

<script>
  export default {}
</script>

<style scoped lang="scss">
    .mainTitle {
        font-size: 15px;
    }
    .test {
        display: grid;
        grid-template-columns: repeat(3,50px);
        grid-template-rows: repeat(5,30px);
        display: flex;
        a {
            display: block;
        }
    }
</style>