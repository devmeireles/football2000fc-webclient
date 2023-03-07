<template>
  <v-carousel hide-delimiters show-arrows="hover" height="180">
    <template v-for="(item, index) in trophies">
      <v-carousel-item v-if="(index + 1) % columns === 1 || columns === 1" :key="index">
        <v-row class="flex-nowrap px-sm-6">
          <template v-for="(n, i) in columns">
            <template v-if="(+index + i) < trophies.length">
              <v-col :key="i">
                <v-sheet v-if="(+index + i) < trophies.length">
                  <div class="d-flex flex-column justify-center align-center pa-6">
                    <div>
                      <img :src="trophies[index + i].image" :alt="trophies[index + i].name" />
                    </div>
                    <div>
                      <p>{{ trophies[index + i].name }}</p>
                    </div>
                  </div>
                </v-sheet>
              </v-col>
            </template>
          </template>
        </v-row>
      </v-carousel-item>
    </template>
  </v-carousel>
</template>

<script>
import { useDisplay } from 'vuetify'

export default {
  name: 'player-trophies',
  data() {
    return {
      trophies: [
        {
          name: 'Champions League',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/4.png?lm=1520606999'
        },
        {
          name: 'FIFA Club World Cup',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/318.png?lm=1520606999'
        },
        {
          name: 'German',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/10.png?lm=1520606996'
        },
        {
          name: 'Spanish Cup',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/11.png?lm=1520606997'
        },
        {
          name: 'UEFA Super Cup',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/354.png?lm=1520606999'
        },
        {
          name: 'German Cup',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/27.png?lm=1520606999'
        },
        {
          name: 'German Super Cup',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/312.png?lm=1520606999'
        },
        {
          name: 'Spanish Super Cup',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/93.png?lm=1520606999'
        },
        {
          name: 'Footballer of the Year',
          image: 'https://tmssl.akamaized.net/images/titel/medium/4.png?lm=1465908580'
        },
        {
          name: 'UEFA Nations League',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/601.png?lm=1653914395'
        },
        {
          name: 'Copa América',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/106.png?lm=1461847499'
        },
        {
          name: 'English Cup',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/47.png?lm=1520606999'
        },
        {
          name: 'Copa Sudamericana',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/154.png?lm=1520606999'
        },
        {
          name: 'Under-20 World Cup',
          image: 'https://tmssl.akamaized.net/images/erfolge/medium/160.png?lm=1461847499'
        }
      ]
    }
  },
  computed: {
    columns() {
      const { name } = useDisplay()
      switch (name.value) {
        case 'xs':
          return 1;
        case 'sm':
          return 2;
        case 'md':
          return 3
        case 'lg':
        case 'xl':
          return 5
        case 'xxl':
          return 6
      }
    }
  },
}
</script>