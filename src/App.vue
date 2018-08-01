<template>
  <v-app dark>
    <v-navigation-drawer persistent :mini-variant="miniVariant" v-model="drawer" enable-resize-watcher app>
      <v-list>
        <v-list-tile v-for="(item, i) in items" :key="i" value="true">
          <v-list-tile-action>
            <v-icon class="white--text" v-html="item.icon"></v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title class="white--text" v-text="item.title"></v-list-tile-title>
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
                  <v-card-media src="http://www.discoverhongkong.com/eng/images/see-do/highlight-attractions/large/1.1.1.11-Lan-Kwai-Fong_03b.jpg" height="200px">
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">Lan Kwai Fong</h3>
                      <div>Lan Kwai Fong is one of Hong Kong’s most popular nightlife hot spots and home to over 90 restaurants and bars.</div>
                    </div>
                  </v-card-title>
                  <v-card-actions>
                    <v-dialog v-model="dialog" persistent>
                      <v-btn color="orange" flat slot="activator">Share</v-btn>
                      <v-card>
                        <v-card-title class="headline">Use Google's location service?</v-card-title>
                        <v-card-text>Let Google help apps determine location. This means sending anonymous location data to Google, even when no apps are running.</v-card-text>
                        <v-card-actions>
                          <v-spacer></v-spacer>
                          <v-btn color="green darken-1" flat @click.native="dialog = false">Disagree</v-btn>
                          <v-btn color="green darken-1" flat @click.native="dialog = false">Agree</v-btn>
                        </v-card-actions>
                      </v-card>
                    </v-dialog>
                    <v-btn flat color="orange">Explore</v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
              <v-flex xs12 sm6 lg4>
                <v-card>
                  <v-card-media src="http://www.discoverhongkong.com/eng/images/see-do/highlight-attractions/large/1.1.1.8-Temple-Street-Night-Market_01.jpg" height="200px">
                  </v-card-media>
                  <v-card-title primary-title>
                    <div>
                      <h3 class="headline mb-0">Temple Street Night Market</h3>
                      <div>
                        Souvenirs, snacks, opera singers and fortune tellers – ordered chaos in action.
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
      <span>&copy; 2018</span>
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
      drawer: false,
      fixed: false,
      items: [
        { icon: 'home', title: 'Home' },
        { icon: 'face', title: 'User' }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Travel App One+',
      dialog: false
    }
  }
}
</script>
