<template>
    <main>
        <WhatWeDo />
        <GrowYourBusiness />
        <CarouselLatestWork />
        <OurPricing />
        <LatestPosts />
        <WhatPeopleSay />
        <ServicesOffered />
    </main>
</template>

<script>
import { store } from '../store.js'
import WhatWeDo from './WhatWeDo.vue';
import GrowYourBusiness from './GrowYourBusiness.vue';
import CarouselLatestWork from './CarouselLatestWork.vue';
import OurPricing from './OurPricing.vue';
import LatestPosts from './LatestPosts.vue';
import WhatPeopleSay from './WhatPeopleSay.vue';
import ServicesOffered from './ServicesOffered.vue';


export default {
    name: 'AppMain',

    components: {
        WhatWeDo,
        GrowYourBusiness,
        CarouselLatestWork,
        OurPricing,
        LatestPosts,
        WhatPeopleSay,
        ServicesOffered
    },

    data() {

        return {
            store,
        };
    },

    methods: {

    }
}
</script>


<style lang="scss" scoped></style>    