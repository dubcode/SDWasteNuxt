<template>
  <div class="row team__member">
        <div class="ctr">
            <div class="row split-col">
                    <div class="row thumb">
                        <img :src="thumb" :alt="title" />
                    </div>
                    <div class="row content">
                        <h1 class="team__name" v-html="title"></h1>
                        <div class="row" v-html="content"></div>
                    </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.team__member {
  padding-top: 2rem;
}
.team__name {
    color: var(--black);
    font-size: 2.2rem;
    line-height: 1.7rem;
    font-weight: 700;
    margin: 0 0 1rem 0;;
}
.team__job {
  display: block;
    color: var(--primary);
    text-transform: uppercase;
    font-size: 1rem;
    font-weight: 700;
    margin: 0 0 1rem;
}
.thumb {
    margin: 0 0 2rem 0;
}
/* 1200 */
@media only screen and (min-width: 1200px) {

}
</style>
<script>
// Import axios
import axios from 'axios'

// export data
export default {

  // Page Name/Id
  name: 'Job',

  // layout template
  layout: 'default',

  asyncData ({ route, params }) {
    return axios.get(process.env.baseUrl + '/jobs').then((response) => {
      // get route params
      const slug = route.params.slug
      // get response data - Note that you can't access the `this` instance inssluge asyncData
      const allPosts = response.data
      // filter response data by slug
      const filteredPost = allPosts.filter(post => post.slug === slug)
      // get data from index [0]
      const postData = filteredPost[0]
      // return data
      return {
        // returned data
        postData,
        // assign data vars
        title: postData.title.rendered,
        slug: postData.slug,
        content: postData.content.rendered,
        thumb: postData.fimg_url,
      }
    })
  },

}
</script>
