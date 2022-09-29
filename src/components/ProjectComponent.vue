<template>
    <section id="projects">
        <div className='subheading tc f2 pa2 ma5'>PROJECTS</div>
        <div className="tc flex justify-center flex-wrap container">

            <article className="center mw6 mw7-ns br3 hidden ba b--black-10 mv4 shadow-1 bg-1">
                <h1 className="f4 bg-near-white br3 br--top black-60 mv0 pv2 ph3">
                    Shopey App
                </h1>
                <div className="pa3 bt b--black-10">
                    <div class="dtc v-top">
                        <img :src="shopey" alt="A bright blue sky" class="db" />
                    </div>
                    <p className="f6 f5-ns lh-copy">
                        Quickly capture what’s on your mind and create your shopping list . Speak a voice memo on the go
                        and have it automatically transcribed. Shopey makes it easy to capture a list for yourself, and
                        share it with friends and family.
                    </p>
                    <div>
                        <h4>Shop what’s on your mind</h4>
                        <ul class="tl">
                            <li>Add lists, items to Shopey. Pressed for time? Record a voice List and Shopey will
                                transcribe it.</li>
                            <li>Share shopping list with friends and family</li>
                        </ul>
                    </div>
                    <div class="tc">
                        <li class="dib mr1 mb2 ma2 grow">
                            <a target="_blank" href="https://play.google.com/store/apps/details?id=com.D2R2.shopey"
                                class="f6 f5-ns b db pa2 link dim dark-gray ba b--black-20">See Live
                            </a>
                        </li>
                    </div>
                </div>
            </article>

            <article className="center mw6 mw7-ns br3 hidden ba b--black-10 mv4 shadow-1 bg-2">
                <h1 className="f4 bg-near-white br3 br--top black-60 mv0 pv2 ph3">
                    Distributed Multi-Camera Synchronization
                </h1>
                <div className="pa3 bt b--black-10">
                    <div class="dtc v-top">
                        <img :src="multi" alt="A bright blue sky" class="db" />
                    </div>
                    <p className="f6 f5-ns lh-copy">
                        Advanced video-based surveillance is required which can assist security personnel by providing
                        reliable real-time alerts and to support efficient video analysis.
                        Cameras can be considered as the nodes in 3D space and by using distance vector algorithm the
                        nearest neighbor graph is created. Purpose of this NN graph is to minimize the global search.
                        Whenever a camera node detects a person, it will extract the features and face of that person.
                        Every node will have a local database in order to re-identify the person.
                    </p>
                    <div class="tc">
                        <li class="dib mr1 mb2 ma2 grow">
                            <a target="_blank" href="https://github.com/sureshkumarjha/Distributed-Multi-Camera-Synchronization"
                                class="f6 f5-ns b db pa2 link dim dark-gray ba b--black-20">Source Code
                            </a>
                        </li>
                    </div>
                </div>
            </article>

            <article className="center mw6 mw7-ns br3 hidden ba b--black-10 mv4 shadow-1 bg-3">
                <h1 className="f4 bg-near-white br3 br--top black-60 mv0 pv2 ph3">
                    Covid Vaccination Management
                </h1>
                <div className="pa3 bt b--black-10">
                    <div class="dtc v-top">
                        <img :src="covid" alt="A bright blue sky" class="db" />
                    </div>
                    <p className="f6 f5-ns lh-copy">
                        Developed application for Covid Vaccination tracking for patients. This project was
                        an assignment for Angular training in TCS. Stack: Angular 9, Firebase
                    </p>
                    <div class="tc">
                        <li class="dib mr1 mb2 ma2 grow">
                            <a target="_blank" href="https://github.com/sureshkumarjha/ng-tcs-assignment/tree/main/08-08-2021%20Day%2007/vaccination-schedule-system"
                                class="f6 f5-ns b db pa2 link dim dark-gray ba b--black-20">Source Code
                            </a>
                        </li>
                        <li class="dib mr1 mb2 ma2 grow">
                            <a target="_blank" href="https://angular-test-70a6d.web.app/home"
                                class="f6 f5-ns b db pa2 link dim dark-gray ba b--black-20">See Live
                            </a>
                        </li>
                    </div>
                </div>
            </article>

            <article className="center mw6 mw7-ns br3 hidden ba b--black-10 mv4 shadow-1 bg-4">
                <h1 className="f4 bg-near-white br3 br--top black-60 mv0 pv2 ph3">
                    MultiPlayer TIC-TAC-TOE
                </h1>
                <div className="pa3 bt b--black-10">
                    <div class="dtc v-top">
                        <img :src="reactg" alt="A bright blue sky" class="db" />
                    </div>
                    <p className="f6 f5-ns lh-copy">
                        TIC-TAC-TOE game with multiplayer feature. Tech Stack : React js, Node, ExpressJs
                    </p>
                    <div class="tc">
                        <li class="dib mr1 mb2 ma2 grow">
                            <a target="_blank" href="https://github.com/sureshkumarjha/ReactGames"
                                class="f6 f5-ns b db pa2 link dim dark-gray ba b--black-20">Cliet Source Code
                            </a>
                        </li>
                        <li class="dib mr1 mb2 ma2 grow">
                            <a target="_blank" href="https://github.com/sureshkumarjha/ReactGames-Server"
                                class="f6 f5-ns b db pa2 link dim dark-gray ba b--black-20">Server Source Code
                            </a>
                        </li>
                    </div>
                </div>
            </article>

            <article className="center mw6 mw7-ns br3 hidden ba b--black-10 mv4 shadow-1 bg-5">
                <h1 className="f4 bg-near-white br3 br--top black-60 mv0 pv2 ph3">
                    Smart Meter
                </h1>
                <div className="pa3 bt b--black-10">
                    <div class="dtc v-top">
                        <img :src="smartmeter" alt="A bright blue sky" class="db" />
                    </div>
                    <p className="f6 f5-ns lh-copy">
                        Developing a smart meter (Non-invasive) which takes reading of power. Using that data we are
                        further implementing regression for prediction and classification for classifying appliances
                        used.
                    </p>
                </div>
            </article>
        </div>
    </section>
</template>
<script>
import shopey from "../assets/projects/Shopey.png";
import smartmeter from "../assets/projects/smartmeter.jpg";
import multi from "../assets/projects/multi.jpg";
import reactg from "../assets/projects/reactg2.jpg";
import covid from "../assets/projects/covid.jpg";
export default {
    name: "ProjectComponent",
    data() {
        return {
            shopey: shopey,
            smartmeter: smartmeter,
            multi: multi,
            reactg: reactg,
            covid: covid
        }
    }
}
</script>
<style>
.bg-1 {
    background-color: #e4ff0033;
}
.bg-2{
    background-color: #0087ff21;
}
.bg-3{
    background: #9f9fff70;
}
.bg-4{
    background: #b3ff9f63
}
.bg-5 {
    background-color: #e4ff0033;
}
</style>