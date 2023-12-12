<script>
import { store } from "../store.js"
export default {
    name: "AppMainSecond",
    data() {
        return {
            store,
            cards: [
                {
                    date: 'july 4, 2019',
                    author: 'by Paul',
                    title: 'Canadian Consulting Firm acquired by UK Giant',
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a ...',
                    img: 'public/startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg',

                },
                {
                    date: 'july 4, 2019',
                    author: 'by Paul',
                    title: 'Canadian Consulting Firm acquired by UK Giant',
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a ...',
                    img: 'public/business-people-working-together-on-project-and-5FHSKBL-1390.jpg',
                }
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="blog-wrapper">
            <div class="square"></div>
            <h3>BLOG</h3>
        </div>
        <div class="recent-wrapper">
            <h2>THE RECENT NEWS YOU MUST READ IT</h2>
            <button>VIEW ALL</button>
        </div>
        <div class="card-wrapper">
            <div class="img-wrapper" v-for="info in cards">
                <div class="positioner">
                    <img :src="info.img" alt="">

                </div>
                <div class="card">
                    <span>{{ info.date }}</span>
                    <div class="border"></div>
                    <span>{{ info.author }}</span>
                    <h3>{{ info.title }}</h3>
                    <p>{{ info.text }}</p>
                </div>

            </div>

        </div>

    </section>
</template>

<style scoped lang="scss">
section {
    margin: 12rem 0;
    padding: 1rem;

    button {
        padding: 1rem 3rem;
        background-color: #39FFBF;
        border: none;

    }

    button:hover {
        background-color: crimson;
        color: white;
    }
}

h2 {
    font-size: 45px;
    color: white;
}

.square {
    width: 50px;
    height: 3px;
    background-color: #39FFBF;
    margin-right: 1rem;
}

.blog-wrapper {
    display: flex;
    align-items: baseline;
    margin-bottom: 1.2rem;

    h3 {
        letter-spacing: 2.8px;
        color: white;
        font-weight: 50;
    }
}

.recent-wrapper {
    display: flex;
    justify-content: space-between;
}

.img-wrapper {
    perspective: 1000px;
    width: 49%;

}

.img-wrapper img {
    width: 100%;
    transform: scale(1);

}

img:hover {

    transition: all 0.3s linear;
    transform: scale(1.05)
}

.card-wrapper {
    margin-top: 4rem;
    display: flex;
    justify-content: space-between;
    width: 100%;
}

.card {
    position: absolute;
    padding: 3rem 6rem;
    right: 0;
    bottom: -6rem;
    width: 590px;
    height: 320px;
    background-color: white;

    h3 {
        font-size: 25px;
    }

    span {
        color: crimson;
        margin-right: 0.25rem;
    }
}

.img-wrapper:hover .card {
    transition: all 0.3s linear;
    bottom: -7rem;
    background-color: #39FFBF;
}

.border {
    display: inline-block;
    height: 12px;
    width: 2px;
    background-color: rgb(255, 255, 255);
    margin: 0 0.5rem;
}


.positioner {
    position: relative;
    overflow: hidden;

}
</style>