<template>

    <div id="mainMenu">

         <v-layout>
         <v-flex xs12 sm10 offset-sm1>
         <v-card id="mainCard">

        <v-img>
        <v-carousel id="mainCarousel">
            <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            ></v-carousel-item>
        </v-carousel>
        </v-img>
        <v-text>
           <h2 id="mainText">
               There are 100 civics questions on the naturalization test. During your naturalization interview, you will be asked up to 10 questions from the list of 100 questions. You must answer correctly six (6) of the 10 questions to pass the civics test.
               </h2>
        </v-text>
       <v-actions>
        <v-bottom-nav
            :active.sync="bottomNav"
            :value="true"
            fixed
            color= #e9e0d8
        >
            <v-btn
                href="/all"
                color="indigo"
                flat
                value="all"
            >
                <span>All</span>
                <v-icon>grade</v-icon>
            </v-btn>

            <v-btn
                href="/government"
                color="indigo"
                flat
                value="americanGov"
            >
                <span>Government</span>
                <v-icon>flag</v-icon>
            </v-btn>

            <v-btn
                href="/history"
                color="indigo"
                flat
                value="americsnHist"
            >
                <span>History</span>
                <v-icon>import_contacts</v-icon>
            </v-btn>

            <v-btn
                href="/integrated"
                color="indigo"
                flat
                value="integratedCiv"
            >
                <span>Integrated Civics</span>
                <v-icon>public</v-icon>
            </v-btn>

        </v-bottom-nav>
        </v-actions>

        </v-card>
        </v-flex>
        </v-layout>

    </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          src: '/img/americanGov.jpg'
        },
        {
          src: '/img/americanHist.jpg'
        },
        {
          src: '/img/integratedCiv.jpg'
        },
        {
          src: '/img/allQ.jpg'
        }
      ],
      bottomNav: 'recent'
    }
  },
  methods: {

  }

}
</script>

<style>
#mainMenu{
    display: flex;
    justify-content: center;
    height: auto;
}
#mainCarousel{
    height: 55vh !important;
}
#mainCard{
    height: auto;
    background-color: #e9e0d8;
    margin-top: 3vh;
}
#mainText{
    height: auto;
    margin: 2vh;
    padding: 2vh;
    font-size: calc(1vh + 1vw);
    font-family: 'Roboto', sans-serif
}
.theme--light.v-bottom-nav .v-btn:not(.v-btn--active) {
    color: #3f51b5 !important
}

</style>
