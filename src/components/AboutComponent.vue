<template>
    <section id="about" className='about-margin section flex justify-center theme-light-blue-bg'>
        <div>
            <div className='subheading tc f2 pa2 '>My Journey so far</div>

            <div className="flex justify-center  aboutparent">

                <div className="aboutblock container ">
                    <!-- <div className="flex"><span>Name :</span> <span>Suresh Jha</span></div>
                    <div className="flex"><span>DOB:</span> <span>March 22, 1999</span></div>
                    <div className="flex"><span>Zip code :</span> <span>400080</span></div>
                    <div className="flex"><span>Email :</span> <span>ronaldo@gmail.com</span></div>
                    <div className="flex"><span>Phone : </span> <span>+1-2234-5678-9-0</span></div> -->
                    <img :src="avtar"  width="450" alt="A bright blue sky" className='br4' />
                    <div class="lh-title pa2 mt1">
                        <span class="f6 b">Favorite Song</span> <br />
                        <span class="ml0">Devil Got My Woman - Skip James</span>
                    </div>
                    <div>
                        <span class="f6 b mt2">Favorite Movie</span><br />
                        <span class="ml0">Primer</span>
                    </div>
                    <div>
                        <span class="f6 b mt2">Favorite Artist</span><br />
                        <span class="ml0">Kanye West</span>
                    </div>
                    <div>
                        <span class="f6 b mt2">Favorite Food</span><br />
                        <span class="ml0">Cheese Pizza</span>
                    </div>
                    <div>
                        <span class="f6 b mt2">Least Favorite Flavor</span><br />
                        <span class="ml0">Cherry</span>
                    </div>
                </div>

                <div className="block">
                    <TimelineComponent />
                </div>

            </div>
        </div>
    </section>
</template>

<script>
import avtar from "../assets/avtar.jpg";
import profile from "../assets/suresh.jpg";
import TimelineComponent from "./TimelineComponent.vue";
export default {
    name: "AboutComponent",
    data() {
        return {
            avtar: avtar,
            profile: profile
        };
    },
    components: { TimelineComponent }
}
</script>

<style scoped>
.about-margin {
    margin: 1px;
}

.aboutblock {
    margin: 2em;
}

.aboutblock div {
    padding: 0.5em;
}

.aboutblock div span {
    width: calc(100% - 130px);
    font-size: 20px;
    line-height: 1.8;
    font-weight: 400;
    color: #999;
}

.aboutblock div span:first-child {
    font-size: 10;
    font-weight: 1000;
    color: #000;
    width: 130px;
}

.block {
    display: flex;
    justify-content: flex-end;
}

@media only screen and (max-width: 600px) {
    .block {
        display: block;
    }

    .aboutparent {
        display: flex;
        flex-wrap: wrap;
    }

    .container {
        margin-right: 1em;
        margin-left: 1em;
    }
}
</style>