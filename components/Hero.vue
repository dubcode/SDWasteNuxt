<template>
      <div class="row hero" :class="heroClass" :lazy-background="heroBg">
        <div class="row hero__bg">
            <div class="ctr">
                <div class="row">
                    <div class="row">
                        <h1>
                            <span>{{ heroTitleOne }}</span>
                            <span>{{ heroTitleTwo }}</span>
                        </h1>
                    </div>
                    <div class="row hero__excerpt">
                      <div v-html="heroExcerpt"></div>
                    </div>
                    <div class="row hero__buttons" v-if="heroButtonOneUrl">
                        <a v-if="heroButtonOneUrl" :href="heroButtonOneUrl" :class="heroButtonOneClass" :target="heroButtonOneTarget">
                          {{ heroButtonOneText }}
                        </a>
                        <a v-if="heroButtonTwoUrl" :href="heroButtonTwoUrl" :class="heroButtonTwoClass" :target="heroButtonTwoTarget">
                          {{ heroButtonTwoText }}
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style>
.hero {
  background: rgb(20,102,54);
  height: 60vh;
  min-height: 600px;
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
.hero__page {
  height: 44vh;
  min-height: 400px;
}
.hero__bg {
  /* background: rgb(20,102,54);
  background: linear-gradient(90deg, rgba(20,102,54,0.7) 10%, rgba(20,102,54,0) 100%); */
  background: rgba(0, 0, 0, 0.3);
  height: 100%;
  width: 100%;
}
.hero .ctr {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
.hero h1 {
    margin: 0 0 2rem 0;
}
.hero h1 span {
  font-family: "Montserrat", sans-serif;
  font-size: 2.2rem;
  line-height: 1;
  font-weight: 700;
  text-transform: uppercase;
  color: #fff;
  display: block;
}

.hero__excerpt {
  color: #fff;
}

.hero__excerpt p {
  max-width: 600px;
  font-size: 1rem;
  line-height: 1.5;
  font-weight: 500;
  margin: 0 0 2rem 0;
}

.hero__excerpt a {
  color: #fff;
  text-decoration: none;
}

.hero__buttons {
  font-weight: 600;
  font-family: "Montserrat", sans-serif;
}

.hero__buttons .button:nth-child(1) {
  margin: 0 0 1rem 0;
}
/* 768 */
@media only screen and (min-width: 768px) {
  .hero__buttons .button:nth-child(1) {
    margin: 0 1rem 0 0;
  }
}
/* 1200 */
@media only screen and (min-width: 1200px) {
    .hero h1 span {
        font-size: 2.8rem;
    }
    .hero p {
        
        font-size: 1.3rem;
    }
}
</style>
<script>
export default {
  name: 'hero',
  // props
  props: [
    // eslint-disable-next-line vue/require-prop-types
    'heroBg',
    'heroClass',
    'heroTitleOne',
    'heroTitleTwo',
    'heroExcerpt',
    'heroButtonOneText',
    'heroButtonOneUrl',
    'heroButtonOneClass',
    'heroButtonOneTarget',
    'heroButtonTwoText',
    'heroButtonTwoUrl',
    'heroButtonTwoClass',
    'heroButtonTwoTarget'
  ]
}
</script>

