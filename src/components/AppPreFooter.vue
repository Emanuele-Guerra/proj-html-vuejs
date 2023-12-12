<script>
import { store } from "../store.js"
export default {
    name: "AppPreFooter",
    data() {
        return {
            store,

        }
    }
}
</script>

<template>
    <section>
        <img src="public/business-people-working-together-on-project-and-B3MZ4TX.jpg" alt="">
        <div class="wrapper">
            <h2>LET'S TALK ABOUT WORK</h2>
            <p>A wonderful serenity has taken possession Far far <br> away, behind the word mountains.</p>
            <button>GET STARTED</button>
        </div>
    </section>
</template>

<style scoped lang="scss">
section {
    text-align: center;
    width: 100%;
    position: relative;
    color: white;

    img {
        z-index: -3;

    }
}

.wrapper {
    width: 600px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    h2 {
        font-size: 45px;
    }


    button {
        margin-top: 2rem;
        padding: 1rem 3rem;
        background-color: greenyellow;
        border: none;
        font-size: 20px;
    }
}
</style>