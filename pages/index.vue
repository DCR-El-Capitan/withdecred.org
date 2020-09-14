<template>
  <div class="background">
    <el-container class="container text--align-center">
      <el-main class="mb-5">
        <el-row>
          <div>
            <img
              src="@/assets/logo/decred-logo.png"
              alt="Decred logo"
              class="nav-logo mb-0"
            />
            <div class="title">withDecred<span class="dot">.</span>org</div>
            <div class="subtitle">Stakeholder-Governed Sound Money</div>
          </div>
        </el-row>

        <el-row :gutter="24">
          <el-col :lg="24" :sm="24" :xs="24">
            <el-card class="card">
              <div slot="header" class="m--flex">
                <h3 class="card-title">
                  <i class="el-icon-magic-stick" />
                  Preface - Decred, an under the radar cryptocurrency
                </h3>
                <!-- <div class="ml-auto">
                  <i class="el-icon-check card--is-done" />
                </div> -->
              </div>
              <p>
                Cryptocurrencies and the digital currency space, in accordance to public perception, is a niche
                field that has a high barrier to entry. This perception is mostly attributable to the fact that the technology 
                is relatively new, and unique to traditional financial products. Much like the oldest child blazes the trail for their younger
                siblings, the team leading the @withdecred initiative has been around the cryptocurrency/blockchain space
                for quite some time, first stumbled upon Bitcoin like most others, and is now fully acclimated and embracing the new and under the radar 
                juggernaut - Decred: Short for "Decentralized Credits"
              <p>
                This website has been envisioned as a map to your personal understanding and future acquisition of Decred. Given Decred is a blockchain based 
                cryptocurrency, and Bitcoin is technically the worlds first application of the novel "blockchain", you will be provided a brief history of money 
                and blockchain 101, however, this website only scratches the surface on these concepts and is tailored for those who already have a basic knowledge 
                and understanding of the world's first blockchain: Bitcoin.
              <p> 
                Decred builds upon the promise of Bitcoin: the idea of self-sovereignty for your money. Decred takes everything that works with Bitcoin (there is no 
                sense in recreating the wheel) and elegantly iterates the model to be more forward looking, inclusive, adaptable, and secure. 
              <p> 
                Make no mistake. The truth is: the majority of cryptocurrency projects are scams, ponzis, and try and use popular jargon to make promises they don't plan 
                on keeping. DeFi, Yield Farming, Governance, Decentralized - all sound great but the reality is these concepts are very hard to get right and the marjority 
                of projects have a few big token holders trying to sell you on these terms to ultimately get rich quick, maintain power and control, and not deliver anything of 
                value. There is no such thing as a free lunch! Promises of 50x and 100x by next week are almost always too good to be true. 
              <p> 
                Decred is in the slim minority of projects that consistently delivers on promises, is built to last, and is positioned to take the main stage as a powerhouse in the
                the cryptocurrency space. We are sold on Decred and this community driven website and initiative is to provide readers and believers with the fundamental knowledge, resources, 
                and support to simplify what we know to be a complex but extremely valuable project: The Decred Project. 
              <p> 
                Are you @withdecred? Dive right into Decred 101 by clicking next below. 
              </p>

              <div class="mt-3 mb-2">
                <nuxt-link to="/a/decred-101">
                  <el-button type="primary" class="huge-cta">
                    Continue reading Decred 101 <i class="el-icon-right"></i>
                  </el-button>
                </nuxt-link>
              </div>
              <!-- <div class="card-footer">
                <i class="el-icon-timer mr-1" /> 6 minutes
              </div> -->
            </el-card>
          </el-col>
        </el-row>

        <el-row :gutter="24">
          <el-col :lg="8" :sm="8" :xs="24">
            <el-card class="card">
              <div slot="header" class="m--flex">
                <h3 class="card-title">
                  <i class="el-icon-connection" />
                  Hybrid Consensus
                </h3>
                <div class="ml-auto">
                  <i class="el-icon-lock" />
                </div>
              </div>
              Learn how Decred's 2-level consensus is ±41x more secure than
              traditional Proof-of-Work blockchains such as Bitcoin or Ethereum.
              <div class="mt-3 mb-4">
                <el-button
                  v-if="!isArticleHybridConsensusUnlocked"
                  disabled
                  size="medium"
                  type="primary"
                >
                  <i class="el-icon-lock mr-1"></i> Article locked
                </el-button>

                <nuxt-link
                  v-if="isArticleHybridConsensusUnlocked"
                  to="/a/decred-hybrid-consensus"
                >
                  <el-button size="medium" type="primary">
                    Read more <i class="el-icon-right ml-1"></i>
                  </el-button>
                </nuxt-link>
              </div>
              <div class="card-footer">
                <i class="el-icon-timer mr-1" /> 8 minutes
              </div>
            </el-card>
          </el-col>

          <el-col :lg="8" :sm="8" :xs="24">
            <el-card class="card">
              <div slot="header" class="m--flex">
                <h3 class="">
                  <i class="el-icon-data-analysis" />
                  Staking &amp; Governance
                </h3>
                <div class="ml-auto">
                  <i class="el-icon-lock" />
                </div>
              </div>
              Learn how you can stake $DCR, earn 8% per anum and vote in
              Decred's governance. Unlike Bitcoin, you can influence how the
              protocol will evolve.
              <div class="mt-3 mb-4">
                <el-button
                  v-if="!isArticleStakingAndGovernanceUnlocked"
                  disabled
                  size="medium"
                  type="primary"
                >
                  <i class="el-icon-lock mr-1"></i> Article locked
                </el-button>

                <nuxt-link
                  v-if="isArticleStakingAndGovernanceUnlocked"
                  to="/a/decred-staking-and-governance"
                >
                  <el-button size="medium" type="primary">
                    Read more <i class="el-icon-right ml-1"></i>
                  </el-button>
                </nuxt-link>
              </div>
              <div class="card-footer">
                <i class="el-icon-timer mr-1" /> 6 minutes
              </div>
            </el-card>
          </el-col>

          <el-col :lg="8" :sm="8" :xs="24">
            <el-card class="card">
              <div slot="header">
                <h3 class="card-title">
                  <i class="el-icon-magic-stick" />
                  What's next (future)
                </h3>
              </div>
              Explore exciting new things coming - Decentralized Exchange,
              Lightning network and unique privacy implementation Coinshuffle++.
              <div class="mt-3 mb-4">
                <el-button
                  v-if="!isArticleWhatsNextUnlocked"
                  disabled
                  size="medium"
                  type="primary"
                >
                  <i class="el-icon-lock mr-1"></i> Article locked
                </el-button>

                <nuxt-link
                  v-if="isArticleWhatsNextUnlocked"
                  to="/a/decred-whats-next"
                >
                  <el-button size="medium" type="primary">
                    Read more <i class="el-icon-right ml-1"></i>
                  </el-button>
                </nuxt-link>
              </div>
              <div class="card-footer">
                <i class="el-icon-timer mr-1" /> 7 minutes
              </div>
            </el-card>
          </el-col>
        </el-row>
      </el-main>
    </el-container>
  </div>
</template>

<script lang="ts">
import Vue, { PropOptions } from 'vue'
import Logo from '~/components/Logo.vue'

export default Vue.extend({
  layout: 'homepage',

  components: {
    Logo,
  },

  data() {
    return {
      isArticleHybridConsensusUnlocked: false,
      isArticleStakingAndGovernanceUnlocked: false,
      isArticleWhatsNextUnlocked: false,
    }
  },

  mounted() {
    this.isArticleHybridConsensusUnlocked = Boolean(
      localStorage.getItem('withdecred:article:hybrid-consensus')
    )
    this.isArticleStakingAndGovernanceUnlocked = Boolean(
      localStorage.getItem('withdecred:article:staking-and-governance')
    )
    this.isArticleWhatsNextUnlocked = Boolean(
      localStorage.getItem('withdecred:article:whats-next')
    )
  },
})
</script>

<style lang="scss" scoped>
.background {
  background-image: url('../assets/images/bg-waves.png');
  background-image: url('../assets/images/bg-waves.webp');
  background-position-y: -70px;
}

.nav-logo {
  height: 50px;
}

.card {
  position: relative;
  text-align: left;

  &--is-done {
    color: $color-secondary-green;
  }

  p + p {
    margin-top: 12px;
  }

  ul li {
    margin-bottom: 8px;
  }

  .huge-cta {
    padding: 20px 30px;
    font-size: 16px;
    font-weight: 500;
  }
}

.card-title {
  font-weight: 500;
  font-size: 20px;
  text-align: left;
}

.card-footer {
  position: absolute;
  bottom: 12px;
  left: 16px;
  font-size: 0.9em;
}

.title {
  display: block;
  color: $font-color-light;
  font-weight: 400;
  font-size: 52px;
  letter-spacing: 0.025em;

  @include media('<=sm') {
    font-size: 48px;
  }
}

.subtitle {
  font-weight: 300;
  font-size: 28px;
  color: $font-color-light;
  margin-bottom: 32px;

  @include media('<=sm') {
    font-size: 22px;
  }
}

.dot {
  // color: $color-primary-blue;
  // color: $color-secondary-lightblue;
  color: $color-secondary-green;
}

.links {
  padding-top: 15px;
}

.my-5 {
  margin: 20px 0;
}
</style>
