<template>
    <div class="timeline">
        <div class="container left">
            <div class="content grow shadow-3">
                <h2 class="fw9">TATA CONSULTANCY SERVICES</h2>
                <h4 class="o-60">July 2021 - Present | Mumbai, MH</h4>
                <p>SOFTWARE ENGINEER</p>
            </div>
        </div>
        <div class="container right">
            <div class="content grow shadow-3">
                <h2 class="fw9">ABN AMRO BANK - ORDER PROCESSING</h2>
                <h4 class="o-60">Feb 2021 - Present | Role: Devops Engineer</h4>
                <p>
                    vai TATA CONSULTANCY SERVICES
                <ul>
                    <li>Adopted Devops way of working and migrated applications
                        from on-premises IBM CMS to public cloud Azure FSCP 3.0 with new enhancements</li>
                    <li>Implemented PingFederate Oauth 2.0
                        Authorization code flow and Client credential flow in application.</li>
                </ul>
                </p>
            </div>
        </div>
        <div class="container left">
            <div class="content grow shadow-3">
                <h2 class="fw9">MANPOWERGROUP USA- EXPERIS 2.0</h2>
                <h4 class="o-60">July 2021 – Feb 2022| Role: Developer</h4>
                <p>
                    vai TATA CONSULTANCY SERVICES
                <ul>
                    <li>Developed new screens and rest services for Inheritance feature using
                        Angular 9, Springboot and SQL</li>
                    <li>Improved code quality and optimized the UI & deployment and testing of the system including unit
                        testing</li>
                </ul>
                </p>
            </div>
        </div>
        <div v-for="(data,index) in timelineData" :key="index">
            <div class="container" :class="{ 'right' : (index%2==leftStart) , 'left' : !(index%2==leftStart)}">
                <div class="content grow shadow-3" >
                    <h2 class="fw9">{{data.title}}</h2>
                    <h4 class="o-60">{{data.subheading}}</h4>
                    <p>{{data.description}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { timelineData } from '@/data';
export default {
    name: "TimelineComponent",
    data() {
        return {
            timelineData: timelineData,
            leftStart: false
        }
    }
}
</script>

<style scoped>
/* The actual timeline (the vertical ruler) */
.timeline {
    position: relative;
    max-width: 1100px;
    margin: 0.5em;
}

/* The actual timeline (the vertical ruler) */
.timeline::after {
    content: '';
    position: absolute;
    width: 6px;
    background-color: white;
    top: 0;
    bottom: 0;
    left: 56%;
    margin-left: -3px;
}

/* Container around content */
.container {
    padding: 10px 40px;
    position: relative;
    background-color: inherit;
    width: 50%;
}

/* The circles on the timeline */
.container::after {
    content: '';
    position: absolute;
    width: 25px;
    height: 25px;
    right: -17px;
    background-color: white;
    border: 4px solid #FF9F55;
    top: 15px;
    border-radius: 50%;
    z-index: 1;
}

/* Place the container to the left */
.left {
    left: 0;
}

/* Place the container to the right */
.right {
    left: 50%;
}

/* Add arrows to the left container (pointing right) */
.left::before {
    content: " ";
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    right: 30px;
    border: medium solid white;
    border-width: 10px 0 10px 10px;
    border-color: transparent transparent transparent white;
}

/* Add arrows to the right container (pointing left) */
.right::before {
    content: " ";
    height: 0;
    position: absolute;
    top: 22px;
    width: 0;
    z-index: 1;
    left: 30px;
    border: medium solid white;
    border-width: 10px 10px 10px 0;
    border-color: transparent white transparent transparent;
}

/* Fix the circle for containers on the right side */
.right::after {
    left: -16px;
}

/* The actual content */
.content {
    padding: 20px 30px;
    background-color: white;
    position: relative;
    border-radius: 6px;
    white-space: pre-line;
}

/* Media queries - Responsive timeline on screens less than 600px wide */
@media screen and (max-width: 600px) {

    /* Place the timelime to the left */
    .timeline::after {
        left: 31px;
    }

    /* Full-width containers */
    .container {
        width: 100%;
        padding-left: 50px;
        padding-right: 10px;
        margin-right: 1em;
        margin-left: 0em;
    }

    /* Make sure that all arrows are pointing leftwards */
    .container::before {
        left: 40px;
        border: medium solid white;
        border-width: 10px 10px 10px 0;
        border-color: transparent white transparent transparent;
    }

    /* Make sure all circles are at the same spot */
    .left::after,
    .right::after {
        left: 15px;
    }

    /* Make all right containers behave like the left ones */
    .right {
        left: 0%;
    }
}
</style>