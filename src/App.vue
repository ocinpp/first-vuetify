<template>
  <v-app light>
    <v-navigation-drawer persistent :mini-variant="miniVariant" v-model="drawer" enable-resize-watcher app>
      <v-list>
        <v-list-tile v-for="(item, i) in items" :key="i" value="true">
          <v-list-tile-action>
            <v-icon light v-html="item.icon"></v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"></v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar fixed app>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title v-text="title"></v-toolbar-title>
    </v-toolbar>
    <main>
      <v-content>
        <v-container fluid grid-list-lg>
          <v-slide-y-transition mode="out-in">
            <v-layout row wrap>
              <v-flex xs12 sm6 lg4>
                <v-card>
                  <v-card-media src="https://vuetifyjs.com/static/doc-images/cards/desert.jpg" height="200px">
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">Kangaroo Valley Safari</h3>
                      <div>Located two hours south of Sydney in the <br>Southern Highlands of New South Wales, ...</div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <v-btn flat color="orange">Share</v-btn>
                    <v-btn flat color="orange">Explore</v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
              <v-flex xs12 sm6 lg4>
                <v-card>
                  <v-card-media src="https://vuetifyjs.com/static/doc-images/cards/docks.jpg" height="200px">
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">Top 10 Australian beaches</h3>
                      <div>
                        <span class="grey--text">Number 10</span><br>
                        <span>Whitehaven Beach</span><br>
                        <span>Whitsunday Island, Whitsunday Islands</span>
                      </div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <v-btn flat color="orange">Share</v-btn>
                    <v-btn flat color="orange">Explore</v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
              <v-flex xs12 sm6 lg4>
                <v-card>
                  <v-card-media src="https://www.discoverhongkong.com/ca/images/see-do/highlight-attractions/large/1.1.1.3-Ladies%27-Market_03.jpg" height="200px">
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">Ladies' Market</h3>
                      <div>About a kilometre of street-market bustle and clothing, accessories and souvenir bargains</div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <v-btn flat color="orange">Share</v-btn>
                    <v-btn flat color="orange">Explore</v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
              <v-flex xs12 sm6 lg4>
                <v-card>
                  <v-card-media src="http://www.discoverhongkong.com/ca/images/see-do/highlight-attractions/large/1.1.1.4-Clock-Tower_03b.jpg" height="200px">
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">Clock Tower</h3>
                      <div>A landmark from the Age of Steam and a reminder of Hong Kong’s colonial heritage</div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <v-btn flat color="orange">Share</v-btn>
                    <v-btn flat color="orange">Explore</v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
              <v-flex xs12 sm6 lg4>
                <v-card>
                  <v-card-media src="http://www.discoverhongkong.com/ca/images/see-do/highlight-attractions/large/1.1.1.6-Tsim-Sha-Tsui-Promende_03.jpg" height="200px">
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">Tsim Sha Tsui Promenade</h3>
                      <div>Take a walk on the bright side! Stroll along the waterfront with your eyes locked on one of the world’s most spectacular city skylines.</div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <v-btn flat color="orange">Share</v-btn>
                    <v-btn flat color="orange">Explore</v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
              <v-flex xs12 sm6 lg4>
                <v-card>
                  <v-card-media src="http://www.discoverhongkong.com/ca/images/see-do/highlight-attractions/large/1.1.1.2-Peak_03a.jpg" height="200px">
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">The Peak</h3>
                      <div>Out-of-this-world view of skyscrapers, the glittering harbour and the green hills of the distant New Territories</div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <v-btn flat color="orange">Share</v-btn>
                    <v-btn flat color="orange">Explore</v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
            </v-layout>
          </v-slide-y-transition>
        </v-container>
      </v-content>
    </main>
    <v-navigation-drawer temporary :right="right" v-model="rightDrawer" app>
      <v-list>
        <v-list-tile @click.native="right = !right">
          <v-list-tile-action>
            <v-icon light>compare_arrows</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-footer :fixed="fixed" app>
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

<<style scoped>
  .card {
    height: 100% !important;
  }
</style>


<script>
export default {
  data() {
    return {
      drawer: true,
      fixed: false,
      items: [
        { icon: 'home', title: 'Home' },
        { icon: 'face', title: 'User' }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Travel App One'
    }
  }
}
</script>
