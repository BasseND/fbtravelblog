<template>
  <section class="container">
    <div>
      <nuxt-link v-for="post in posts" :key="post.id" to="post.id">
        <article class="post-preview">
          <v-card>
            <v-img :src="post.thumbnailUrl" aspect-ratio="2.75"></v-img>

            <v-card-title primary-title>
              <div>
                <h3 class="headline mb-0">{{ post.title }}</h3>
                <div>
                  <p>{{ post.previewText }}</p>
                </div>
              </div>
            </v-card-title>

            <v-card-actions>
              <v-btn flat color="orange">Share</v-btn>
              <v-btn flat color="orange">Explore</v-btn>
            </v-card-actions>
          </v-card>

        </article>

      </nuxt-link>

    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        {
          title: "A big adventure in Paris",
          previewText: "A la découverte de la ville de Paris.",
          thumbnailUrl:
            "http://www.parisetudiant.com/uploads/assets/evenements/verso_fiche/2017/11/117741_la-grande-roue-a-paris-place-de-la-concorde.jpg",
          id: "323"
        },
        {
          title: "A big adventure in Paris",
          previewText: "A la découverte de la ville de Paris.",
          thumbnailUrl:
            "http://www.parisetudiant.com/uploads/assets/evenements/verso_fiche/2017/11/117741_la-grande-roue-a-paris-place-de-la-concorde.jpg",
          id: "223"
        }
      ]
    };
  }
};
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

