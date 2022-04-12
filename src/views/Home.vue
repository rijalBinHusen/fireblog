<template>
  <div class="home">
    <Blogpost :post="welcomeScreen" />
    <Blogpost :post="post" v-for="post in sampleBlogPost" :key="post.title" />
  </div>
</template>

<script>
import Blogpost from "../components/BlogPost.vue"

export default {
  name: "Home",
  components: {
    Blogpost
  },
  data() {
    return {
      welcomeScreen: {
        title: "Welcome!",
        blogPost:
          "Weekly blog articles with all things programming including HTML, CSS, JavaScript and more. Register today to never miss a post!",
        welcomeScreen: true,
        photo: "coding",
      },
      sampleBlogPost: [
        {
          title: "This is the title of the blog",
          blogHTML: "This is the blog content",
          blogCoverPhoto: "beautiful-stories",
        },
        {
          title: "This is the 2 of blog title",
          blogHTML: "This is the 2 of blog content",
          blogCoverPhoto: "designed-for-everyone",
        }
      ],
    }
  }
};
</script>
