<template>
    <div class="row mission">
        <div class="ctr">
            <h2>{{ missionTitle }}</h2>
            <div class="flex">
              <div class="row">
                <p v-html="missionExcerpt"></p>
              </div>
            </div>
            <div class="flex">
                <img src="/images/cn-logo.jpg" height="169" width="294" alt="logo">
            </div>
            <div class="row mission__button">
                <div class="flex">
                    <nuxt-link :to="missionButtonUrl" class="button button-dark">
                      {{ missionButtonTitle }}
                    </nuxt-link>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.mission {
  background: #f7f7f7;
  padding: 8rem 0;
  text-align: center;
}
.mission h2 {
  color: #146636;
  text-transform: uppercase;
  font-size: 2.4rem;
  line-height: 2.8rem;
  margin: 0 0 2rem 0;
  font-weight: 600;
  font-family: "Montserrat", sans-serif;
}
.mission p {
  color: #146636;
  max-width: 768px;
  font-size: 1.2rem;
  line-height: 1.9rem;
  margin: 0 auto 2rem auto;
}

.mission p:last-child {
  margin: 0 auto;
}

.mission img {
  display: block;
  margin: 0 auto 2rem auto;
  height: auto;
  max-width: 160px;
}

.page-mission .mission img,
.page-mission .mission__button {
  display: none;
}
</style>
<script>
export default {
  name: 'mission',
  // props
  props: [
    // eslint-disable-next-line vue/require-prop-types
    'missionTitle',
    'missionExcerpt',
    'missionButtonTitle',
    'missionButtonUrl'
  ]
}
</script>

