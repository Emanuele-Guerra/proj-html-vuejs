<script>
import { store } from "../store.js"

export default {

    name: "AppConsultant",
    data() {
        return {
            store,
            cards: [
                {
                    icon: "fa-solid fa-chart-line",
                    title: 'STATISTICAL CONSULTING',
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a'
                },
                {
                    icon: "fa-solid fa-bullhorn",
                    title: 'DIGITAL CONSULTING',
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a'
                },
                {
                    icon: "fa-solid fa-wallet",
                    title: 'BANKING CONSULTING',
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a'
                },
                {
                    icon: "fa-solid fa-bullseye",
                    title: 'ENTERPRISE CONSULTING',
                    text: 'When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a'
                }
            ]
        }
    },

}
</script>

<template>
    <section>
        <div class="wrapper">
            <div class="title-wrap">
                <h2>OUR CONSULTANTS CAN HELP YOU</h2>
                <div class="likeAnHr"></div>
            </div>
            <div class="flex-cards">
                <div class="card" v-for="infos in cards">
                    <div class="title-icon">
                        <div class="icon-wrap"><i :class="infos.icon"></i></div>
                        <h3>{{ infos.title }}</h3>
                    </div>
                    <div class="paragraph">
                        <P>{{ infos.text }}</P>

                    </div>
                </div>
            </div>



        </div>
    </section>
    <div class="underwrapper">
        <div>
            <img src="public/business-people-working-together-on-project-and-5FHSKBL.jpg" alt="">
        </div>
        <div class="text-cont">
            <div class="about-us">
                <div class="Asquare"></div>
                <h3>ABOUT US</h3>
            </div>
            <div>
                <h2>WE MAKE YOUR STRATEGY WORK</h2>
                <p>When, while lovely valley teems with vapour around meand
                    eridian sun strikes the upper impenetrable foliage of my trees,
                    and but a thousand unknown plants are noticed when I hear the buzz
                    of the little world among the stalks,and grow familiar indescribable
                    forms of the insects .and flies, then I feel the presence of the Almighty . </p>
            </div>
        </div>
    </div>

    <div class="end-wrapper">
        <div class="f-content">
            <h3>WE HELP TO DELIVER THE BUSINESS CASE</h3>
        </div>
        <div class="f-content">
            <p>When, while lovely valley teems with vapour
                around meand meridian sun strikes the upper impenetrable
                foliage of my trees, and but a thousand unknown</p>
        </div>
        <button>GET STARTED</button>
    </div>
</template>


<style scoped lang="scss">
section {
    display: flex;
    justify-content: flex-end;
    margin-top: 13rem;
    width: 100%;

}

h2 {
    font-size: 30px;
}

.title-wrap {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.likeAnHr {
    width: 760px;
    height: 3px;
    background-color: aqua;
}

.wrapper {
    width: 97%;
    background-color: white;
    padding-bottom: 10rem;

    .title-wrap {
        padding: 6rem 0 0 10rem;
    }
}

.card {
    display: flex;
    flex-direction: column;
    padding: 6rem 0 0 10rem;
    width: calc(90% / 2);

    h3 {
        font-size: 25px;
    }


}

.paragraph {
    width: 80%;
    padding-left: 7rem;
}

.title-icon {
    display: flex;
    align-items: flex-start;
}

.icon-wrap {
    display: inline-block;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-size: 30px;
    width: 4rem;
    height: 4rem;
    border-radius: 50%;
    background-color: red;
    margin-right: 3rem;
}



.flex-cards {
    display: flex;
    flex-wrap: wrap;
}

.underwrapper {
    display: flex;
    align-items: center;

    h2 {
        font-size: 60px
    }

    img {
        width: 900px;
        height: 610px;
        object-fit: cover;
    }
}

.about-us {
    display: flex;
    align-items: center;
}

.Asquare {
    width: 45px;
    height: 3px;
    background-color: aqua;
    margin-right: 1rem;
}

.text-cont {
    padding: 3.5rem;
    color: white;
}

.end-wrapper {
    position: relative;
    width: 97%;
    background-color: aquamarine;
    display: flex;
    align-items: center;
    justify-content: space-around;
    padding: 7rem 12rem 7rem 8rem;

    h3 {
        font-size: 35px;
    }

    button {
        padding: 1.5rem 3rem;
        background-color: greenyellow;
        border: none;
        font-size: 20px;
        position: absolute;
        bottom: 0;
        right: 0;
    }

    .f-content {
        width: 37%;
    }
}
</style>
