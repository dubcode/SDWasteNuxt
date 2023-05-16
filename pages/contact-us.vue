<template>
  <div class="row">
    <Hero
      hero-class="hero__page"
      :hero-bg="hero_background"
      :hero-title-one="hero_title_one"
      :hero-title-two="hero_title_two"
      :hero-excerpt="hero_excerpt"
      :hero-button-one-text="hero_button_one_text"
      :hero-button-one-url="hero_button_one_url"
      :hero-button-one-class="hero_button_one_class"
      :hero-button-one-target="hero_button_one_target"
    />
    <div class="row">
        <div class="ctr">
            <div class="row two-col two-col__contact">
                <div class="row content">
                    <h1 class="content__title">SD Waste Paper Recycling Centre</h1>
                    <div v-html="page_content"></div>
                </div>
                <div class="row contact__sidebar">
                  <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d32851.63836283205!2d-2.247809126934673!3d53.52006086006569!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487bb05bb9eeb2d1%3A0x53e41fdd8a729fcb!2sSD%20Waste%20Paper%20Recycling%20Centre!5e0!3m2!1sen!2suk!4v1684174924980!5m2!1sen!2suk" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>
<style scoped>
.two-col__contact {
  gap: 0 4rem;
}
.contact__sidebar {
  display: flex;
}
.contact__sidebar iframe {
  height: 100%;
  float: left;
  width: 100%;
}
</style>
<script>
// Import axios
import axios from 'axios'

// export data
export default {

  // Page Name/Id
  name: 'Contact',

  // layout template
  layout: 'default',

  // SSR asyncData Request
  asyncData () {
    return axios.get(process.env.baseUrl + '/pages/13301?_embed').then((response) => {
      // get response data - Note that you can't access the `this` instance inside asyncData
      const page = response.data
      console.log(page)
      // return data
      return {
        // returned data
        page,

        // meta vars
        seo_title: page.yoast_head_json.title,
        seo_desc: page.yoast_head_json.og_description,

        // content
        page_title: page.title.rendered,
        page_subtitle: page.acf.page_sub_title,
        page_content: page.content.rendered,

        // hero one
        hero_background: page.acf.hero.background,
        hero_title_one: page.acf.hero.title_one,
        hero_title_two: page.acf.hero.title_two,
        hero_excerpt: page.acf.hero.excerpt,
        hero_button_one_text: page.acf.hero.button_one_title,
        hero_button_one_url: page.acf.hero.button_one_url,
        hero_button_one_class: page.acf.hero.button_one_class,
        hero_button_one_target: page.acf.hero.button_one_target,

      }
    })
  },

  head () {
    return {
      title: this.seo_title,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.seo_desc
        },
        {
          hid: 'og:title',
          name: 'og:title',
          content: this.seo_title
        },
        {
          hid: 'og:description',
          name: 'og:description',
          content: this.seo_desc
        }
      ]
    }
  }

}
</script>
