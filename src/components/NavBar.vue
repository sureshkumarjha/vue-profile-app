<template>
    <nav>
        <div>
            <header className="bg-black fixed w-100 ph3 pv3 ph3-m ph4-l header">
                <nav className="f6 fw6 ttu tracked">
                    <span className='dim white f4 pointer' @click="openNav">&#9776;</span>
                </nav>
            </header>

            <div id="mySidenav" className="sidenav">
                <div className='flex flex-column justify-center'>
                    <div className="closebtn" @click="closeNav">&times;</div>
                    <div @click="closeNav('about')">About</div>
                    <div @click="closeNav('projects')">Projects</div>
                    <div @click="closeNav('contact')">Contact</div>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
    name: "NavBar",
    methods: {
        openNav() {
            console.log("Open Nav");
            document.getElementById("mySidenav").style.height = "100%";
        },
        closeNav(e) {
            let ele = document.getElementById(e);
            if (ele !== null) {
                ele.scrollIntoView({
                    block: 'start',
                    behavior: 'smooth',
                    inline: 'start'
                });
            }
            document.getElementById("mySidenav").style.height = "0";
        }
    }
}
</script>

<style scoped>
.header {
    z-index: 2;
    opacity: 1;
    display: flex;
    justify-content: flex-end;
}
</style>