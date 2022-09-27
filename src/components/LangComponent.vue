<template>
    <div class="mb4 bg-lang br4 shadow-1">
        <div class="b pa2 tc">
            <h3>Languages I know</h3>
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
    name: 'LangComponent',
    computed: {
        images() {
            const path = require.context('./../assets/icons/lang', false, /\.png$/);
            return path.keys().map(path).reverse();
        }
    }
}
</script>

<style>
.bg-lang{
    background: #9f9fff70;
}
</style>