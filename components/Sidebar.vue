<template>
    <div class="row sidebar">
        <h3>Recycling Services</h3>
        <ul class="sidebar__nav">
            <li>
                <nuxt-link to="/paper-recycling/">
                    Paper Recycling
                </nuxt-link>
            </li>
            <li>
                <nuxt-link to="/cardboard-recycling/">
                    Cardboard Recycling
                </nuxt-link>
            </li>
            <li>
                <nuxt-link to="/plastic-recycling/">
                    Plastic Recycling
                </nuxt-link>
            </li>
            <li>
                <nuxt-link to="/confidential-waste-destruction/">
                    Confidential Waste
                </nuxt-link>
            </li>
            <li>
                <nuxt-link to="/office-clearance/">
                    Office Clearance
                </nuxt-link>
            </li>
        </ul>
        <div class="sidebar__icons">
          <ul>
            <li>
              <a href="tel:01617407466" title="Call 01617407466">
                <div class="sidebar__icons-thumb">
                  <img src="/images/svg/tel.svg" height="18" width="18" alt="telephone-icon" data-not-lazy />
                </div>
                <div class="sidebar__icons-cta">
                  <span>0161 740 7466</span>
                </div>
              </a>
            </li>
            <li>
              <a href="mailto:office@sdwaste.co.uk" title="Email office@sdwaste.co.uk" target="_blank">
                <div class="sidebar__icons-thumb">
                  <img src="/images/svg/email.svg" height="18" width="18" alt="email-icon" data-not-lazy />
                </div>
                <div class="sidebar__icons-cta">
                  <span>office@sdwaste.co.uk</span>
                </div>
              </a>
            </li>
          </ul>
        </div>
        <nuxt-link to="/meet-the-team/" class="sidebar__banner">
          <h6 class="sidebar__banner-title">
            Meet The Team
          </h6>
          <div class="sidebar__banner-thumb">
            <img src="/images/team.jpg" alt="Meet The Team" data-not-lazy />
          </div>
        </nuxt-link>
    </div>
</template>
