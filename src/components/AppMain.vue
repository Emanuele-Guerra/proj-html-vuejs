<script>
import { store } from "../store.js"

export default {
    name: "AppMain",
    data() {
        return {
            store,
            carousel: [
                {
                    path: ''
                },
                {
                    path: ''
                },
                {
                    path: ''
                },
            ]
        }
    },

}
</script>

<template>
    <div class="d-flex project">
        <div class="square"></div>
        <h3>PROJECT</h3>
    </div>
    <section>
        <div class="wrapper">
            <div>
                <h2>OUR EXPERT TRUSTED CONSULTANTS HELP CLIENTS</h2>
            </div>
            <div class="d-flex">
                <div class=" arrow-box"><i class="fa-solid fa-arrow-left"></i></div>
                <div class=" arrow-box"><i class="fa-solid fa-arrow-right"></i></div>
            </div>
        </div>
        <div class="carousel-wrapper">
            <!-- <img src="" alt=""> //path dinamico img -->
        </div>





    </section>
</template>

<style scoped lang="scss">
section {
    padding: 1rem;
    color: white;
}

.d-flex {
    display: flex;
}

.square {
    width: 40px;
    height: 3px;
    background-color: aquamarine;
    margin-right: 1rem;
}

.wrapper {
    display: flex;
    justify-content: space-between;
}

.project {
    align-items: center;
    padding: 1rem;
}

.arrow-box {
    padding: 1rem 1.2rem;
    background-color: rgb(68, 68, 68);
    margin: 0.2rem;
}
</style>