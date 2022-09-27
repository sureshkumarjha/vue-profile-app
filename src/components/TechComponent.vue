<template>
    <div class="mb4 bg-tech br4 shadow-1">
        <div class="b pa2 tc">
            <h3>Tools & Technologies I use</h3>
        </div>
        <div class="flex flex-wrap  justify-center">
            <div class="ma2 grow" v-for="image in images" :key="image">
                <img :src="image" fluid width="80" />
            </div>
        </div>
    </div>
</template>
  
<script>
export default {
    name: 'TechComponent',
    computed: {
        images() {
            const path = require.context('./../assets/icons', false, /\.png$/);
            return path.keys().map(path).reverse();
        }
    }
}
</script>

<style>
.bg-tech{
    background: #b3ff9f63
}
</style>