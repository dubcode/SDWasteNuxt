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
        <div class="row">
          <div class="row content">
            <h2 class="content__subtitle" v-html="page_subtitle"></h2>
            <div v-html="page_content"></div>
          </div>
          <div class="row team">
            <ul>
              <li v-for="post in posts" :key="post.id">
                <nuxt-link :to="{ path: '/jobs/' + post.slug }">
                  <img :src="post.fimg_url" :alt="post.title.rendered" />
                  <div class="row team__excerpt">
                    <div class="row team__excerpt-block">
                      <span class="team__name" v-html="post.title.rendered"></span>
                    </div>
                  </div>
                </nuxt-link>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.team h1 {
    color: #146636;
    text-transform: uppercase;
    font-size: 2.4rem;
    line-height: 2.8rem;
    font-weight: 700;
    margin: 0 0 2rem 0;
    text-align: center;
}

.team__excerpt {
  padding: 0 1rem;
}

.team__excerpt-block {
  background: #fff;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
  border-bottom: 3px solid #fff;
  padding: 1rem;
  transform: translateY(-2rem);
  transition: all ease-out 0.3s
}

.team li:hover .team__excerpt-block {
  border-bottom: 3px solid var(--primary);
  transform: translateY(-3rem);
}

.team__job {
    color: var(--primary);
    text-transform: uppercase;
    font-size: 1rem;
    font-weight: 700;
    margin: 0 0 0.5rem;
}

.team__name {
    color: var(--black);
    font-size: 1.6rem;
    line-height: 1.7rem;
    font-weight: 700;
    margin: 0;
}
.team ul,
.team li {
    list-style-type: none;
    margin: 0;
    padding: 0;
}
.team li {
    margin: 0 0 2rem 0;
}
.team li a,
.team li span {
    display: block;
}
.team li a {
    color: var(--primary);
    font-size: 1.2rem;
    font-weight: 600;
    text-decoration: none;
}
.team li img {
    display: block;
    height: auto;
    width: 100%;
    margin: 0 0 1rem 0;
}

/* 768 */
@media only screen and (min-width: 768px) {
    .team ul {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        gap: 4rem;
        grid-auto-flow: row;
    }
    @media all and (-ms-high-contrast:none) {
        .team ul {
            display: -ms-grid;
            -ms-grid-columns: 1fr 1fr;
            -ms-grid-rows: 1fr 1fr;
        }
    }
    .team li {
        margin: 0;
    }
}

/* 1200 */
@media only screen and (min-width: 1200px) {
    .team ul {
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 1fr;
    }
    @media all and (-ms-high-contrast:none) {
        .team ul {
            display: -ms-grid;
            -ms-grid-columns: 1fr 1fr 1fr;
            -ms-grid-rows: 1fr;
        }
    }
}
</style>
<script>
// Import axios
import axios from 'axios'

// export data
export default {

  // Page Name/Id
  name: 'Jobs',

  // layout template
  layout: 'default',

  // data
  data () {
    return {
      posts: {},
      page: null,
      page_title: null,
      page_subtitle: null,
      page_content: null,
      hero_background: null,
      hero_title_one: null,
      hero_title_two: null,
      hero_excerpt: null,
      hero_button_one_text: null,
      hero_button_one_url: null,
      hero_button_one_class: null,
      hero_button_one_target: null
    }
  },

  methods: {

    // get posts method
    getPosts () {
        axios.get(process.env.baseUrl + '/jobs')
        .then((response) => {
          this.posts = response.data
        })
        .catch((response) => {
          console.log(response)
        })
    },

    // get page content method
    getPage () {
        axios.get(process.env.baseUrl + '/pages/13309?_embed')
        .then((response) => {
          this.page = response.data
          this.page_title = this.page.title.rendered
          this.page_subtitle = this.page.acf.page_sub_title
          this.page_content = this.page.content.rendered
          this.hero_background = this.page.acf.hero.background
          this.hero_title_one = this.page.acf.hero.title_one
          this.hero_title_two = this.page.acf.hero.title_two
          this.hero_excerpt = this.page.acf.hero.excerpt
          console.log(this.page)
        })
        .catch((response) => {
          console.log(response)
        })
    },

  },

  // created
  created () {
    this.getPosts()
    this.getPage()
  }

}
</script>
