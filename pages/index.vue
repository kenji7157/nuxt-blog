<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <logo />
      </div>
      <v-card>
        <v-card-title class="headline">
          Welcome to the Nuxt.js template
        </v-card-title>
        <v-card-text>
          <div v-for="(content, index) in contents" :key="index" class="origin">
            <hr />
            作成日：{{ content.createdAt }} <br />
            タイトル：{{ content.title }} <br />
            本文：{{ content.body }}
          </div>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import axios from 'axios'
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo,
  },

  async asyncData() {
    const res = await axios.get(
      // your-service-id部分は自分のサービスidに置き換えてください
      'https://kk-nuxt-blog.microcms.io/api/v1/article',
      {
        // your-api-key部分は自分のapi-keyに置き換えてください
        headers: { 'X-API-KEY': '63a41b21-d7d6-4bdb-a1f5-3f9e5865f71b' },
      }
    )
    const contents = res.data.contents
    console.log('dataの確認', res.data.contents)
    return { contents }
  },
}
</script>
