<template>
  <div class="background">
    <!-- <el-main class="my-6"> </el-main> -->

    <div class="background--alt">
      <!-- <ContentNav>
        <label>Navigation</label>
        <nuxt-link to="/a/decred-101">
          Decred 101
        </nuxt-link>
        <nuxt-link to="/a/decred-sound-money">
          Decred & Sound Money
        </nuxt-link>
        <nuxt-link to="/a/decred-hybrid-consensus">
          Hybrid Consensus
        </nuxt-link>
        <nuxt-link to="/a/decred-staking-governance">
          Staking & Governance
        </nuxt-link>
        <nuxt-link to="/a/decred-whats-next">
          What's Next?
        </nuxt-link>
        <nuxt-link to="/a/decred-purchase">
          <i class="el-icon-coin" /> Purchase $DCR
        </nuxt-link>
      </ContentNav> -->

      <div class="container">
        <el-main class="article mt-20 mb-6">
          <el-row :gutter="24">
            <el-col :lg="16" :xs="24">
              <h1 class="article--title">Hybrid Consensus</h1>

              <NavButtonGroup class="mt-5">
                <nuxt-link to="/a/decred-101">
                  <NavButton prependIcon="back">
                    <template v-slot:label>
                      <i class="el-icon-magic-stick" /> Decred 101 - Start here
                    </template>
                    Previous article
                  </NavButton>
                </nuxt-link>
                <nuxt-link to="/a/decred-staking-and-governance">
                  <NavButton appendIcon="right">
                    <template v-slot:label>
                      <i class="el-icon-magic-stick" /> Staking & Governance
                    </template>
                    Next article
                  </NavButton>
                </nuxt-link>
              </NavButtonGroup>

              <div class="hr my-5" />

              <p>
                In a nutshell, Decred's hybrid PoW/PoS consensus system was
                designed from the ground up to solve
                <a
                  href="https://blog.companyzero.com/2015/11/bitcoins-biggest-challenges/"
                  target="_blank"
                  class="underline"
                  >Bitcoin's biggest challenges</a
                >
                .
              </p>

              <p>
                Each new block on the Decred chain goes through a
                <span class="underline"
                  >multi-factor security verification process</span
                >, similar to a 2 factor authentication, before being considered
                fully valid. Similar to Bitcoin, Decred transactions are first
                aggregated by Proof-of-Work miners into new blocks. However, in
                the hybrid consensus model, Decred mined blocks are then
                required to be signed/approved by Proof-of-Stake voters who hold
                tickets (locked DCR), for which 5 tickets (out of ~41,000) are
                pseudorandomly chosen (similar to a lottery) each block to vote.
                This two-step process that mixes both PoW and PoS systems is at
                the core of Decred's hybrid consensus.
              </p>

              <div class="video my-3">
                <iframe
                  width="560"
                  height="315"
                  src="https://www.youtube.com/embed/GAMp5V_gG1E"
                  frameborder="0"
                  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                ></iframe>
              </div>

              <p>
                Instead of issuing 100% of the block reward through the
                Proof-of-Work system (Bitcoin model), newly minted DCR is shared
                between miners, stakeholders, and the Decred Treasury
                (Development Fund) as shown below:
              </p>

              <ul>
                <li>
                  60% to fairly compensate miners who have the biggest running
                  costs
                </li>
                <li>
                  30% to reward those who time-lock DCR to help secure the
                  network
                </li>
                <li>
                  10% is deposited in the Treasury to fund future project
                  development
                </li>
              </ul>

              <p>
                DCR issuance is fixed and known at every point in time. You can
                find additional issuance detail details about it in the
                <a
                  href="https://blog.companyzero.com/2015/11/bitcoins-biggest-challenges/"
                  target="_blank"
                  class="underline"
                  >Decred Documentation</a
                >
              </p>

              <BlockHint>
                Proof-of-Stake voters are the Decred Project decision makers who
                oversee/safeguard the Treasury funds. Currently, there are 6
                million DCR locked in Stakeholder tickets which control a 600K
                DCR or
                <span class="underline">±$10,000,000 USD</span> development
                fund.
              </BlockHint>
            </el-col>
            <el-col :lg="6" :xs="24">
              <!-- <StakeyCard type="explorer" /> -->
            </el-col>
          </el-row>

          <el-row :gutter="24" class="mt-5">
            <el-col :lg="16" :xs="24">
              <h2>Proof-of-Work component</h2>
              <p>
                Proof-of-Work participants commit their computer hardware and
                resources to process network transactions and aggregate
                transactions into the blocks that make up the Decred blockchain.
              </p>

              <p>
                When a miner creates a valid block, they receive the fees from
                all of the transactions included in the block as well as
                <strong>60% of the block reward</strong>.
              </p>

              <p>
                Decred uses the <strong>BLAKE-256</strong> hashing function. PoW
                mining can be done using GPUs, however, more powerful DCR ASICs
                are now available. Since the introduction of ASIC mining, the
                PoW difficulty has become high enough to make GPU mining
                unlikely to be profitable.
              </p>

              <BlockHint>
                While some networks have taken a stance against ASIC mining,
                evidence shows the opposite. ASICs are not only inevitable, but
                desirable: ASIC miners have skin in the game because they can't
                repurpose their hardware.
              </BlockHint>

              <h2>A second layer of security</h2>

              <p>
                In Bitcoin, Ethereum and other pure PoW blockchains, only miners
                can interact with the chain directly. To dilute power, Decred
                combines PoW mining with Proof-of-Stake voting.
              </p>

              <p>
                Decred holders time-lock their DCR to buy tickets, and in each
                block 5 tickets are pseudorandomly selected and called to vote.
                When a ticket is called it makes two kinds of votes:
              </p>

              <ul>
                <li>
                  To approve or reject any open consensus rule change proposals
                </li>
                <li>
                  To approve or reject the regular transaction tree of the
                  previous block
                </li>
              </ul>

              <p>
                PoS voters provide the network with a second layer of security.
                The Decred network double checks every block to protect itself
                against invalid transactions but also against misbehaving
                miners.
              </p>

              <p>
                Ongoing research indicates Decred is up to
                <span class="underline"
                  >40x times more expensive to attack than Bitcoin</span
                >
                and other pure PoW networks given the same hashrate.
              </p>

              <div class="image my-4">
                <img src="@/assets/articles/decred-attack-cost-2.png" />
                <div class="description">
                  Find more information on
                  https://dcrdata.decred.org/attack-cost
                </div>
              </div>

              <BlockHint>
                <p>
                  <strong>When do tickets unlock?</strong> The ticket lottery is
                  pseudorandom. PoS voters commit to locking their funds for a
                  pseudorandom period of time, and it can go on for up to 142
                  days.
                </p>
                <p>
                  This mechanism ensures that
                  <span class="underline"
                    >stakeholders will behave in the network's best
                    interests</span
                  >.
                </p>
              </BlockHint>
            </el-col>

            <el-col :lg="6" :xs="24" type="flex">
              <!-- <StakeyCard /> -->
            </el-col>
          </el-row>

          <el-row>
            <el-col :gutter="24" :lg="16" :xs="24">
              <h2>The Armored Lizard</h2>

              <p>
                Decred's hybrid system makes it abnormally expensive to attack
                the network. Attackers not only need to amass big amounts of
                hashing power but also purchase and stake tickets in order to
                validate the malicious blocks they mine. In this scenario,
                attackers must be highly vested in the network and any attack
                would also compromise their own funds!
              </p>

              <p>
                While the Proof-of-Work system is extensively documented in the
                cryptocurrency space, the addition of a Proof-of-Stake layer and
                its implementation as a governance mechanism is an absolute
                differentiator in the space.
              </p>

              <div class="image my-4">
                <img
                  src="@/assets/articles/decred-cost-of-attack-comparison-1.jpg"
                />
              </div>

              <p>
                In the next article, you'll learn the basics about Decred's
                Staking and Governance system.
              </p>
            </el-col>
          </el-row>

          <el-row>
            <el-col :gutter="24" :lg="16" :xs="24">
              <NavButtonGroup class="mt-5">
                <nuxt-link to="/a/decred-101">
                  <NavButton prependIcon="back">
                    <template v-slot:label>
                      <i class="el-icon-magic-stick" /> Decred 101 - Start here
                    </template>
                    Previous article
                  </NavButton>
                </nuxt-link>
                <nuxt-link to="/a/decred-staking-and-governance">
                  <NavButton appendIcon="right">
                    <template v-slot:label>
                      <i class="el-icon-magic-stick" /> Staking & Governance
                    </template>
                    Next article
                  </NavButton>
                </nuxt-link>
              </NavButtonGroup>
            </el-col>
          </el-row>
        </el-main>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import BlockHint from '@/components/BlockHint/index.vue'
import ContentNav from '@/components/ContentNav/index.vue'
import NavButton from '@/components/NavButton/index.vue'
import NavButtonGroup from '@/components/NavButtonGroup/index.vue'
import StakeyCard from '@/components/StakeyCard/index.vue'

export default Vue.extend({
  components: {
    BlockHint,
    ContentNav,
    NavButton,
    NavButtonGroup,
    StakeyCard,
  },

  mounted() {
    localStorage.setItem('withdecred:article:hybrid-consensus', 'true')
  },
})
</script>

<style lang="scss" scoped>
.background {
  // background-image: url('../assets/images/bg-waves.png');
  background-image: url('../../assets/images/bg-waves.webp');
  background-position-y: -50px;
}

.background--alt {
  background-color: $color-primary-white;
  color: $color-secondary-black;
}

.subpage-card {
  position: absolute;
  // top: -50px;
  top: 0;
  padding: 40px 60px;
  transform: translateY(-50%);
  z-index: 50;

  h1 {
    display: block;
    font-size: 32px;
    font-weight: 500;
    line-height: 1.5;
    // letter-spacing: 0.025em;
    // margin-bottom: 32px;
  }
}

.subpage-card__footer {
  // position: absolute;
  // bottom: 16px;
  font-size: 0.9em;
}
</style>
