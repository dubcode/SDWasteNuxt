<template>
    <div class="row icons">
        <div class="ctr">
            <ul>
                <li>
                    <div>
                    <nuxt-link to="/paper-recycling/">
                        <div class="thumb">
                            <img src="/images/icon5b.png" height="174" width="131" alt="Paper Recycling">
                        </div>
                        <span>Paper Recycling</span>
                    </nuxt-link>
                    </div>
                </li>
                <li>
                    <div>
                    <nuxt-link to="/shredding-overview/">
                        <div class="thumb">
                            <img src="/images/icon3b.png" height="174" width="131" alt="Shredding Services">
                        </div>
                        <span>Shredding Services</span>
                    </nuxt-link>
                    </div>
                </li>
                <li>
                    <div>
                    <nuxt-link to="/cardboard-recycling/">
                        <div class="thumb">
                            <img src="/images/icon7b.png" height="174" width="131" alt="Cardboard Recycling">
                        </div>
                        <span>Cardboard Recycling</span>
                    </nuxt-link>
                    </div>
                </li>
                <li>
                    <div>
                    <nuxt-link to="/plastic-recycling/">
                        <div class="thumb">
                            <img src="/images/icon1b.png" height="174" width="131" alt="Plastic Recycling">
                        </div>
                        <span>Plastic Recycling</span>
                    </nuxt-link>
                    </div>
                </li>
			</ul>
	    </div>
    </div>
</template>
<style>
  .icons {
    background: #fff;
    padding: 2rem 0;
  }
.icons ul {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: minmax(min-content, max-content);
  gap: 1em;
  text-align: center;
  margin: 0;
  padding: 0;
}
.icons li {
  list-style-type: none;
}
.icons li a {
  text-decoration: none;
}
.icons li > div {
  padding: 2rem;
  width: 100%;
}
.icons li .thumb {
  background: #146636;
  border-radius: 100%;
  overflow: hidden;
  height: 160px;
  width: 160px;
  margin: 0 auto 1em auto;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all ease 0.3s;
}
.icons li a:hover .thumb {
  background: #333;
}
.icons .thumb img {
  display: block;
  margin: 0 auto;
  height: 50%;
  width: auto;
  transition: transform ease 0.3s;
  transform: scale(1);
}
.icons li a:hover .thumb img {
  transform: scale(1.15);
}
.icons li span {
  color: #146636;
  text-transform: uppercase;
  font-size: 1.4rem;
  font-weight: 600;
  font-family: "Montserrat", sans-serif;
}
.icons li a:hover span {
  color: #333;
}
/* 768 */
@media only screen and (min-width: 768px) {
    .icons ul {
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    gap: 0;
  }
  .icons li span {
    font-size: 1.2rem;
  }
}
@media only screen and (min-width: 1140px) {
  .icons li span {
    font-size: 1.6rem;
    line-height: 1.7rem;
  }
}
</style>
<script>
export default {
  name: 'icons',
}
</script>

