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
            ],
            veraCard: [
                {
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little .',
                    name: 'Vera Duncan',
                    description: 'Amazon Inc.',
                    path: 'public/oliver-ragfelt-488196-2.jpg'
                },
                {
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little .',
                    name: 'Vera Duncan',
                    description: 'Amazon Inc.',
                    path: 'public/12679.jpg'
                },
                {
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a thousand unknown plants are noticed by when I hear the buzz of the little .',
                    name: 'Vera Duncan',
                    description: 'Amazon Inc.',
                    path: 'public/oliver-ragfelt-488196-unsplash.jpg'
                }

            ]
        }
    }

}
</script>

<template>
    <div class="d-flex project">
        <div class="square"></div>
        <h3>PROJECT</h3>
    </div>
    <section>
        <div class="wrapper">
            <div class="carousel-title">
                <h2>OUR EXPERT TRUSTED CONSULTANTS HELP CLIENTS</h2>
            </div>
            <div class="d-flex arrow-div">
                <div class=" arrow-box"><i class="fa-solid fa-arrow-left"></i></div>
                <div class=" arrow-box"><i class="fa-solid fa-arrow-right"></i></div>
            </div>
        </div>
        <div class="carousel-wrapper">
            <img src="public/DRY-1-790x592.jpg" alt="">
            <img src="public/DRY-1-790x592.jpg" alt="">
            <img src="public/DRY-1-790x592.jpg" alt="">
        </div>
        <div class="flex-project">
            <div class="under-carousel-wrapper">
                <p>TESTIMONIAL</p>
                <div class="square-carousel"></div>
            </div>
        </div>

        <div class="customer-title">
            <div>
                <h2>WHAT'S THE CUSTOMER SAY ABOUT OUR WORK</h2>
            </div>
        </div>
    </section>
    <div class="content-of-cards">
        <div class="card-wrapper">
            <div class="card" v-for="card in veraCard">
                <p class="text">{{ card.text }}</p>
                <h5>{{ card.name }}</h5>
                <p class="desc">{{ card.description }}</p>
                <div class="card-back">
                    <img :src="card.path" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
section {
    padding: 1rem;
    color: white;

    h2 {
        font-size: 45px;
    }
}

.carousel-title {
    width: 900px;
}

.arrow-div {
    height: 3.8rem;
}

.d-flex {
    display: flex;
}

.square {
    width: 50px;
    height: 3px;
    background-color: aquamarine;
    margin-right: 1rem;
}

.wrapper {
    display: flex;
    justify-content: space-between;
}

.project {
    margin-top: 13rem;
    align-items: center;
    padding: 1rem;
    color: white;
    letter-spacing: 2.8px;
}

.arrow-box {
    padding: 1rem 1.2rem;
    background-color: rgb(68, 68, 68);
    margin: 0.2rem;
}

.carousel-wrapper {
    margin-top: 3rem;
    display: flex;
    justify-content: space-between;

    img {
        width: calc(96% / 3);
    }
}

.under-carousel-wrapper {
    width: 55%;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;

    p {
        letter-spacing: 2.8px;
    }


}

.flex-project {
    margin-top: 8rem;
    width: 100%;
    display: flex;
    justify-content: flex-end;

}

.square-carousel {
    width: 50px;
    height: 3px;
    background-color: aquamarine;

}

.customer-title {
    margin-top: 1.8rem;
    display: flex;
    justify-content: flex-end;

    div {
        width: 50%;
        text-align: right;
    }
}

.content-of-cards {
    display: flex;
    justify-content: flex-end;
}

.card-wrapper {
    width: 100%;

    margin: 3rem 0 0 1rem;
    display: flex;


}

.card {
    width: calc(100% / 3);
    height: 400px;
    position: relative;
    background-color: white;
    padding: 4rem;

    .text {
        margin-bottom: 4rem;
    }

    h5 {
        font-size: 25px;
        margin-bottom: 1rem;
    }


}

.card:hover {
    background-color: transparent;
    transition: all 0.3s ease;

    h5 {
        color: white;
    }

    p {
        color: rgb(152, 152, 152);
    }
}

.card-back {
    height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    z-index: -1;

    img {
        height: 100%;
        width: 100%;

    }
}
</style>