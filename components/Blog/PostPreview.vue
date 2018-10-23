<template>

    <nuxt-link to="post.id">
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

</template>

<script>
export default {
  props: {}
};
</script>

<style>
</style>

