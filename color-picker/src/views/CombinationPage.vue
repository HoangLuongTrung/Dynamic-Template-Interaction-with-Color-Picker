<template>
  <div class="combination-page">
    <div
      class="header"
      :style="{ backgroundColor: getCombinationRelated?.combination?.color?.hex }"
    ></div>
    <div class="detail">
      <combination-detail
        v-bind:data-source="getCombinationRelated"
        @select="onSelect($event)"
        @selectRelated="onSelectRelated($event)"
      ></combination-detail>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      combinationSelected: 0,
      combinationColorData: [
        {
          combination: {
            liked: false,
            id: 719,
            slug: 'pastel-blonde',
            color: {
              slug: 'rose-quartz',
              hex: '#F7CAC9',
              name: 'Rose Quartz',
            },
            featuredImage: {
              alt: '',
              url: 'RoseQuartz.png',
            },
            name: 'Pastel Blonde',
            likes: 10953,
            colors: [
              {
                slug: 'yellow',
                hex: '#fff4bd',
                name: 'Yellow',
              },
              {
                slug: 'rose-quartz',
                hex: '#f4b9b8',
                name: 'Rose Quartz',
              },
              {
                slug: 'spearmint',
                hex: '#85d2d0',
                name: 'Spearmint',
              },
              {
                slug: 'purple',
                hex: '#887bb0',
                name: 'Purple',
              },
            ],
          },
          relatedCombinations: [
            {
              id: 1109,
              name: 'Trees in Bloom',
              slug: 'trees-in-bloom',
              colors: ['#f9ccd3', '#aa1945', '#f1ced4', '#391306'],
              likes: 5469,
              liked: false,
            },
            {
              id: 1297,
              name: 'Rosy Dew',
              slug: 'rosy-dew',
              colors: ['#f9f1f0', '#fadcd9', '#f8afa6', '#f79489'],
              likes: 49295,
              liked: true,
            },
            {
              id: 2359,
              name: 'Rosy Afters',
              slug: 'rosy-afters',
              colors: ['#ffc5d0', '#f7d6d0', '#fb6090', '#821d30'],
              likes: 10329,
              liked: false,
            },
            {
              id: 1385,
              name: 'Cherry Blossom Swirl',
              slug: 'cherry-blossom-swirl',
              colors: ['#391306', '#710019', '#f1ced4', '#f9ccd3'],
              likes: 1259,
              liked: false,
            },
            {
              id: 2133,
              name: 'Clusters of Beauty',
              slug: 'clusters-of-beauty',
              colors: ['#d48c70', '#f4b9b8', '#ebbbb0', '#e98980'],
              likes: 10825,
              liked: false,
            },
            {
              id: 656,
              name: 'Sunlit Eggplant',
              slug: 'sunlit-eggplant',
              colors: ['##efd3b5', '#5f093d', '#b21368', '#d67ba8'],
              likes: 3765,
              liked: true,
            },
          ],
        },
        {
          combination: {
            liked: false,
            id: 1297,
            slug: 'rosy-dew',
            color: {
              slug: 'dusty-rose',
              hex: '#DCAE96',
              name: 'Dusty Rose',
            },
            featuredImage: {
              alt: '',
              url: 'dustyrose12.png',
            },
            name: 'Rosy Dew',
            likes: 49295,
            colors: [
              {
                slug: 'cream',
                hex: '#f9f1f0',
                name: 'Cream',
              },
              {
                slug: 'rose-quartz',
                hex: '#fadcd9',
                name: 'Rose Quartz',
              },
              {
                slug: 'dusty-rose',
                hex: '#f8afa6',
                name: 'Dusty Rose',
              },
              {
                slug: 'coral',
                hex: '#f79489',
                name: 'Coral',
              },
            ],
          },
          relatedCombinations: [
            {
              id: 2571,
              name: 'Rosy Flamingo',
              slug: 'rosy-flamingo',
              colors: ['#e8b4b8', '#eed6d3', '#a49393', '#67595e'],
              likes: 47048,
              liked: false,
            },
            {
              id: 1367,
              name: 'Power Up',
              slug: 'power-up',
              colors: ['#000000', '#900020', '#e9ddd4', '#e9ddd4'],
              likes: 2114,
              liked: false,
            },
            {
              id: 2133,
              name: 'Clusters of Beauty',
              slug: 'clusters-of-beauty',
              colors: ['#d48c70', '#f4b9b8', '#ebbbb0', '#e98980'],
              likes: 10825,
              liked: false,
            },
            {
              id: 1292,
              name: 'Rose Petals',
              slug: 'rose-petals',
              colors: ['#3b0404', '#deb3ad', '#de847b', '#b95c50'],
              likes: 6511,
              liked: false,
            },
            {
              id: 1109,
              name: 'Trees in Bloom',
              slug: 'trees-in-bloom',
              colors: ['#f9ccd3', '#aa1945', '#f1ced4', '#391306'],
              likes: 5467,
              liked: false,
            },
          ],
        },
        {
          combination: {
            liked: false,
            id: 1385,
            slug: 'cherry-blossom-swirl',
            color: {
              slug: 'burgundy',
              hex: '#800020',
              name: 'Burgundy',
            },
            featuredImage: {
              alt: '',
              url: 'Burgundy21.png',
            },
            name: 'Cherry Blossom Swirl',
            likes: 1260,
            colors: [
              {
                slug: 'black',
                hex: '#391306',
                name: 'Black',
              },
              {
                slug: 'rose-quartz',
                hex: '#f1ced4',
                name: 'Rose Quartz',
              },
              {
                slug: 'burgundy',
                hex: '#710019',
                name: 'Burgundy',
              },
              {
                slug: 'rose-quartz',
                hex: '#f9ccd3',
                name: 'Rose Quartz',
              },
            ],
          },
          relatedCombinations: [
            {
              id: 2140,
              name: 'Cool Berry Scoop',
              slug: 'cool-berry-scoop',
              colors: ['#ffa3b8', '#f7d6d0', '#fc3c80', '#821d30'],
              likes: 2340,
              liked: false,
            },
            {
              id: 609,
              name: 'Red Beanie Practise Activity',
              slug: 'red-beanie-practise-activity',
              colors: ['#ba0f30', '#2f2440', '#c6b79b', '#ff2511'],
              likes: 4142,
              liked: false,
            },
            {
              id: 393,
              name: 'Petal Party',
              slug: 'petal-party',
              colors: ['#f2c5e0', '#d43790', '#ec8fd0', '#870a30'],
              likes: 7958,
              liked: false,
            },
            {
              id: 498,
              name: 'Buddhist Monk',
              slug: 'buddhist-monk',
              colors: ['#fbdd00', '#e9a200', '#b32800', '#7f0000'],
              likes: 1270,
              liked: false,
            },
            {
              id: 3368,
              name: 'Stepping Stones',
              slug: 'stepping-stones',
              colors: ['#e4e5e8', '#53565a', '#4d0011', '#4b443c'],
              likes: 1248,
              liked: false,
            },
          ],
        },
        {
          combination: {
            liked: false,
            id: 2359,
            slug: 'rosy-afters',
            color: {
              slug: 'hot-pink',
              hex: '#FF69B4',
              name: 'Hot Pink',
            },
            featuredImage: {
              alt: '',
              url: 'Hot_Pink10.png',
            },
            name: 'Rosy Afters',
            likes: 10331,
            colors: [
              {
                slug: 'rose-quartz',
                hex: '#ffc5d0',
                name: 'Rose Quartz',
              },
              {
                slug: 'scallop-seashell',
                hex: '#f7d6d0',
                name: 'Scallop Seashell',
              },
              {
                slug: 'hot-pink',
                hex: '#fb6090',
                name: 'Hot Pink',
              },
              {
                slug: 'rose-red',
                hex: '#821d30',
                name: 'Rose Red',
              },
            ],
          },
          relatedCombinations: [
            {
              id: 1618,
              name: 'Raspberry Cream',
              slug: 'raspberry-cream',
              colors: ['#ae388b', '#5df15d', '#e983d8', '#f9b4f6'],
              likes: 2063,
              liked: false,
            },
            {
              id: 3915,
              name: 'Sweet Cotton Sugar',
              slug: 'sweet-cotton-sugar',
              colors: ['#efebe0', '#fb8da0', '#fb6b90', '#fb4570'],
              likes: 12055,
              liked: false,
            },
            {
              id: 393,
              name: 'Petal Party',
              slug: 'petal-party',
              colors: ['#f2c5e0', '#d43790', '#ec8fd0', '#870a30'],
              likes: 7958,
              liked: false,
            },
            {
              id: 849,
              name: 'Cupcake Delight',
              slug: 'cupcake-delight',
              colors: ['#ebe0d0', '#ec9ec0', '#ff0080', '#a91b60'],
              likes: 9114,
              liked: false,
            },
            {
              id: 2743,
              name: 'Spike of Mint',
              slug: 'spike-of-mint',
              colors: ['#7cf3a0', '#b4f8c8', '#ff75d8', '#ff45b5'],
              likes: 2381,
              liked: false,
            },
          ],
        },
        {
          combination: {
            liked: false,
            id: 2133,
            slug: 'clusters-of-beauty',
            color: {
              slug: 'rose-quartz',
              hex: '#F7CAC9',
              name: 'Rose Quartz',
            },
            featuredImage: {
              alt: '',
              url: 'RoseQuartz_Set6_1.png',
            },
            name: 'Clusters of Beauty',
            likes: 10822,
            colors: [
              {
                slug: 'burnt-sienna',
                hex: '#d48c70',
                name: 'Burnt Sienna',
              },
              {
                slug: 'rose-quartz',
                hex: '#f4b9b8',
                name: 'Rose Quartz',
              },
              {
                slug: 'dusty-rose',
                hex: '#ebbbb0',
                name: 'Dusty Rose',
              },
              {
                slug: 'coral',
                hex: '#e98980',
                name: 'Coral',
              },
            ],
          },
          relatedCombinations: [
            {
              id: 1109,
              name: 'Trees in Bloom',
              slug: 'trees-in-bloom',
              colors: ['#f9ccd3', '#aa1945', '#f1ced4', '#391306'],
              likes: 5462,
              liked: false,
            },
            {
              id: 1297,
              name: 'Rosy Dew',
              slug: 'rosy-dew',
              colors: ['#f9f1f0', '#fadcd9', '#f8afa6', '#f79489'],
              likes: 49276,
              liked: false,
            },
            {
              id: 2359,
              name: 'Rosy Afters',
              slug: 'rosy-afters',
              colors: ['#ffc5d0', '#f7d6d0', '#fb6090', '#821d30'],
              likes: 10324,
              liked: false,
            },
          ],
        },
        {
          combination: {
            liked: false,
            id: 656,
            slug: 'sunlit-eggplant',
            color: {
              slug: 'orchid',
              hex: '#DA70D6',
              name: 'Orchid',
            },
            featuredImage: {
              alt: '',
              url: 'Orchid_Set1_15.png',
            },
            name: 'Sunlit Eggplant',
            likes: 3765,
            colors: [
              {
                slug: 'champagne',
                hex: '#efd3b5',
                name: 'Champagne',
              },
              {
                slug: 'fuchsia',
                hex: '#5f093d',
                name: 'Fuchsia',
              },
              {
                slug: 'fuchsia',
                hex: '#b21368',
                name: 'Fuchsia',
              },
              {
                slug: 'orchid',
                hex: '#d67ba8',
                name: 'Orchid',
              },
            ],
          },
          relatedCombinations: [
            {
              id: 655,
              name: 'Wild Orchid',
              slug: 'wild-orchid',
              colors: ['#005437', '#debad6', '#340744', '#741aac'],
              likes: 2496,
              liked: false,
            },
            {
              id: 128,
              name: 'Icy Gradient',
              slug: 'icy-gradient',
              colors: ['#eeb5eb', '#c26dbc', '#c8f4f9', '#3cacae'],
              likes: 9930,
              liked: false,
            },
            {
              id: 650,
              name: 'Sweet Orchid',
              slug: 'sweet-orchid',
              colors: ['#a3c14a', '#6d8343', '#d103d1', '#6E3562'],
              likes: 681,
              liked: false,
            },
            {
              id: 674,
              name: 'Powder Eye Shadow',
              slug: 'powder-eye-shadow',
              colors: ['#6e3562', '#b464a3', '#cf045a', '#6e676a'],
              likes: 102,
              liked: false,
            },
            {
              id: 691,
              name: 'Pasture of Dreams',
              slug: 'pasture-of-dreams',
              colors: ['#d3b1c2', '#c197d2', '#211522', '#613659'],
              likes: 9129,
              liked: false,
            },
          ],
        },
        {
          combination: {
            liked: false,
            id: 1109,
            slug: 'trees-in-bloom',
            color: {
              slug: 'rose-red',
              hex: '#FF033E',
              name: 'Rose Red',
            },
            featuredImage: {
              alt: '',
              url: 'rosered21.png',
            },
            name: 'Trees in Bloom',
            likes: 5471,
            colors: [
              {
                slug: 'rose-quartz',
                hex: '#f9ccd3',
                name: 'Rose Quartz',
              },
              {
                slug: 'rose-red',
                hex: '#aa1945',
                name: 'Rose Red',
              },
              {
                slug: 'rose-quartz',
                hex: '#f1ced4',
                name: 'Rose Quartz',
              },
              {
                slug: 'puce',
                hex: '#391306',
                name: 'Puce',
              },
            ],
          },
          relatedCombinations: [
            {
              id: 712,
              name: 'Cool Cream Strawberry',
              slug: 'cool-cream-strawberry',
              colors: ['#e7625f', '#c85250', '#f7bec0', '#e9eae0'],
              likes: 5232,
              liked: false,
            },
            {
              id: 2359,
              name: 'Rosy Afters',
              slug: 'rosy-afters',
              colors: ['#ffc5d0', '#f7d6d0', '#fb6090', '#821d30'],
              likes: 10330,
              liked: false,
            },
            {
              id: 1297,
              name: 'Rosy Dew',
              slug: 'rosy-dew',
              colors: ['#f9f1f0', '#fadcd9', '#f8afa6', '#f79489'],
              likes: 49295,
              liked: false,
            },
            {
              id: 1117,
              name: 'Pomegranate Crush',
              slug: 'pomegranate-crush',
              colors: ['#dc4731', '#fff3d9', '#b8390e', '#3b0918'],
              likes: 3225,
              liked: false,
            },
            {
              id: 704,
              name: 'Sweet Frost Lips',
              slug: 'sweet-frost-lips',
              colors: ['#fbe7e0', '#f9e4d0', '#ecc0b0', '#9c3940'],
              likes: 1740,
              liked: false,
            },
          ],
        },
      ],
    }
  },

  computed: {
    getCombinationRelated() {
      console.log('combinationColorData: ', this.combinationColorData)

      if (!this.combinationSelected) {
        return this.combinationColorData[0]
      }
      const isExist = this.combinationColorData.find(
        (item) => item.combination.id === this.combinationSelected,
      )
      if (!isExist) {
        return this.combinationColorData[0]
      }

      return isExist
    },
  },

  methods: {
    onSelect(data) {
      navigator.clipboard.writeText(data.hex).then(() => {
        alert(`Copied: ${data.hex}`)
      })
    },
    onSelectRelated(data) {
      this.combinationSelected = data
      console.log('onSelectRelated: ', data)
    },
  },
}
</script>

<style scoped>
.combination-page {
  min-height: 100vh;
}
.combination-page .header {
  background: url('../assets/images/foreground.png') no-repeat center center;
  background-color: yellow;
  background-size: cover;
  width: 100%;
  height: 300px;
}
</style>
