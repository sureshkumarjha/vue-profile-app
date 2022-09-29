<template>
    <section id="about" className='about-margin section flex justify-center'>
        <div>
            <div className='subheading tc f2 pa2 '>My Journey so far</div>

            <div className="flex justify-center  aboutparent">

                <div className="aboutblock container animate__animated animate__fadeInLeft">
                    <div class="bg-info br4 shadow-1 mb4 tc">
                        <h3 class="tc">So what About me?</h3>
                        <img :src="profile2" class="w-90 br2" alt="A bright blue sky" />
                        <div class="ma2">
                            <p> Hi, I'm Suresh Kumar Jha, I'm <strong _>Full stack Developer</strong> + I love to work
                                on <strong>Project &amp; Ideas</strong> + loves <strong>challenging</strong>
                                assignments.</p>
                            <p>Enthusiastic focused and motivated Junior Developer with <strong>1+ year</strong> of
                                experience is seeking an
                                opportunity to contribute to institutions by implementing concepts, knowledge, and
                                methodologies to learn thereby adding value for the organization. Flexible and adaptable
                                to
                                demands of changing work environments. Team player and also independently responsible.
                            </p>
                            <p> My Life is <strong>LEARN</strong> + <strong>CODE</strong> + <strong>ADVENTURE</strong> +
                                <strong>WATCH</strong> (<strong> SERIES, MOVIES,
                                    ANIME </strong>)+<strong>FITNESS</strong>
                            </p>
                            <div class="tc">
                                <li class="dib mr1 mb2">
                                <a target="_blank"
                                    href="https://drive.google.com/file/d/1K6_u9E8PK4ZJrN2-GvMeIRnuQe1e1S0K/view"
                                    class="f6 f5-ns b db pa2 link dim dark-gray ba b--black-20">Download Resume
                                </a>
                            </li>
                            </div>
                            
                        </div>
                    </div>
                    <LangComponent />
                    <TechComponent />
                    <div class="bg-likes br4 shadow-1 mb4">
                        <div class="lh-title pa2 mt1">
                        <span class="f6 b">Favorite Song</span> <br />
                        <span class="ml0">Frame of Mind - Braken and Tristam</span>
                    </div>
                    <div>
                        <span class="f6 b mt2">Favorite Anime</span><br />
                        <span class="ml0">Naruto</span>
                    </div>
                    <div>
                        <span class="f6 b mt2">Favorite Artist</span><br />
                        <span class="ml0">Selena Gomez</span>
                    </div>
                    <div>
                        <span class="f6 b mt2">Favorite Food</span><br />
                        <span class="ml0">Pav Bhaji</span>
                    </div>
                    </div>


                </div>

                <div className="timeline-block">
                    <TimelineComponent />
                </div>

            </div>
        </div>
    </section>
</template>

<script>
import avtar from "../assets/avtar.jpg";
import profile from "../assets/suresh.jpg";
import profile2 from "../assets/profile2.jpg"
import TimelineComponent from "./TimelineComponent.vue";
import LangComponent from "./LangComponent.vue";
import TechComponent from "./TechComponent.vue";
export default {
    name: "AboutComponent",
    data() {
        return {
            avtar: avtar,
            profile: profile,
            profile2 : profile2
        };
    },
    components: { TimelineComponent, LangComponent, TechComponent }
}
</script>

<style scoped>
.bg-info {
    background-color: #e4ff0033;
}
.bg-likes{
    background-color: #0087ff21;
}

.about-margin {
    margin: 1px;
    width: 100%;
}

.aboutblock {
    margin: 1em;
    width: 30%;
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

.timeline-block {
    display: flex;
    justify-content: flex-end;
}

.aboutparent {
    width: 100%;
}

@media only screen and (max-width: 1000px) {
    .timeline-block {
        display: block;
        width: 100%;
    }

    .aboutblock {
        width: 100%;
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