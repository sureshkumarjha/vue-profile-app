<template>
    <div>
        <span className='f3 pa2 grey'>I'm a </span>
        <b><span className='f2 b underline sliding-text'>{{val}}</span></b>
        <span className='f2 black'>|</span>
    </div>
</template>

<script>
import { rolesList } from '@/data'
export default {
    name: "SlidingTextComponent",
    data() {
        return {
            val: ""
        }
    },
    mounted() {
        let arr = rolesList;
        let i = 0
        let c = 0
        let flag = true
        let delta = 250
        const interval = setInterval(() => {
            if (c < arr[i].length && flag) {
                c = c + 1
            } else {
                c = c - 1
                flag = false
                if (c === 0) {
                    i = i + 1
                    if (i > arr.length - 1) {
                        i = 0
                    }
                    flag = true
                    c = 0
                }
            }
            this.val = arr[i].substring(0, c);
        }, delta);
        return () => clearInterval(interval);
    }
}
</script>

<style>
.sliding-text {
    color: #3e64ff;
}
</style>