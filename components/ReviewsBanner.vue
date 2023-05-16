<template>
    <div class="row reviews-banner">
        <div class="ctr">
            <span class="reviews-banner-title">Google Reviews</span>
            <div class="flex">
                <div class="row">
                    <p>
                        <nuxt-link to="/reviews/">Click here to see our latest reviews on Google.</nuxt-link>
                    </p>
                </div>
            </div>
            <div class="flex">
                <nuxt-link to="/reviews/">
                    <img src="/images/google-ratings-banner.jpg" height="61" width="277" alt="google-reviews-banner" title="Google Reviews Banner" />
                </nuxt-link>
            </div>
        </div>
    </div>
</template>
<style scoped>
.reviews-banner {
  background: rgba(0, 0, 0, 0.015);
  border: 1px solid rgba(0, 0, 0, 0.05);
  padding: 4rem 2rem;
  text-align: center;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
}
.reviews-banner-title {
  color: #666;
  display: block;
  text-transform: uppercase;
  font-size: 1.6rem;
  font-weight: 600;
  font-family: "Montserrat", sans-serif;
  line-height: 1.8rem;
  margin: 0 0 1rem 0;
}
.reviews-banner a {
  color: #666;
  text-decoration: none;
  text-align: center;
}
.reviews-banner p {
  color: #666;
  max-width: 768px;
  font-size: 1.1rem;
  line-height: 1.7rem;
  font-weight: 400;
  margin: 0 auto 2rem auto;
}
.reviews-banner img {
  padding: 5px;
  display: block;
  margin: 0 auto;
  height: auto;
  max-width: 160px;
}
@media only screen and (min-width: 1140px) {
  .reviews-banner p {
    padding: 0 1rem;
  }
}
</style>
<script>
export default {
  name: 'reviews-banner',
}
</script>

