<template>
  <div class="home-page">
    <section class="intro">
      <h1>Get the latest tech news!</h1>
    </section>
    <section class="featured-posts">
      <!-- <nuxt-link :to="'/posts/' + 1"  class="post-preview">
        <article>
          <div class="post-thumbnail" style="background-image: url('http://www.nunnovation.com/wp-content/uploads/2017/09/Tech-Trends-770x300.png')"></div>
          <div class="post-content">
            <h1>Post Title 1</h1>
            <p>Preview Text 1</p>
          </div>
        </article>   
      </nuxt-link>
      <nuxt-link :to="'/posts/' + 2"  class="post-preview">
        <article>
          <div class="post-thumbnail" style="background-image: url('https://orig00.deviantart.net/a8f5/f/2010/204/2/8/abstract_circle_wallpaper_by_tennsoccerdr.jpg')"></div>
          <div class="post-content">
            <h1>Post Title 2</h1>
            <p>Preview Text 2</p>
          </div>
        </article>   
      </nuxt-link> -->

      <PostPreview
        id="1"
        thumbnail="http://www.nunnovation.com/wp-content/uploads/2017/09/Tech-Trends-770x300.png"
        title="Hello there!"
        previewText="This is my first post." />
      <PostPreview
        id="2"
        thumbnail="https://orig00.deviantart.net/a8f5/f/2010/204/2/8/abstract_circle_wallpaper_by_tennsoccerdr.jpg"
        title="Hi there!"
        previewText="This is my second post." />
      <PostPreview
        id="3"
        thumbnail="https://hdwallsource.com/img/2014/7/cool-high-tech-wallpaper-30878-31608-hd-wallpapers.jpg"
        title="Hi techies!"
        previewText="This is my third post." />

    </section>
  </div>
</template>

<script>
  import PostPreview from '@/components/posts/PostPreview'

  export default {
    components: {
      PostPreview
    }
  }
</script>

<style scoped>

.intro {
  height: 300px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~/assets/images/main-page-background.jpg');
  background-position: center;
  background-size: cover;

}

.intro h1 {
  position: absolute;
  top: 10%;
  left: 5%;
  width: 90%;
  font-size: 1.5rem;
  color: black;
  background-color: rgb(211, 211, 211);
  padding: 10px;
  /* border-radius: 10px; */
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid darkgray;
}

@media (min-width: 768px) {
  .intro h1 {
    font-size: 2rem;
  }
}

.featured-posts {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

/* .post-preview {
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
  width: 90%;
}

a {
  text-decoration: none;
  color: black;
}

@media (min-width: 850px) {
  .post-preview {
    width: 400px;
    margin: 10px;
  }
}

.post-thumbnail {
  width: 100%;
  height: 200px;
  background-position: center;
  background-size: cover;
}

.post-content {
  padding: 10px;
  text-align: center;
} */

a:hover .post-content,
a:active .post-content {
  background-color: #ccc;
}

</style>
