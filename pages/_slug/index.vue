<template>
  <div>
    <div v-html="post.contents" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Context } from '@nuxt/types'

export default Vue.extend({
  name: 'SlugPage',
  async asyncData({ $microcms, _params }: Context & any): Promise<any> {
    const post = await $microcms.get({
      // endpoint: `post/${_params.slug}`,
      endpoint: `post/bqwj4f59ec`,
    })
    return {
      post,
    }
  },
})
</script>
