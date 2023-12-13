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
        <img src="/business-people-working-together-on-project-and-B3MZ4TX.jpg" alt="">
        <div class="wrapper">
            <h2>LET'S TALK ABOUT WORK</h2>
            <p>A wonderful serenity has taken possession Far far <br> away, behind the word mountains.</p>
            <button>GET STARTED</button>
        </div>
    </section>
</template>

<style scoped lang="scss">
template {
    margin-top: 5rem;
}

section {

    text-align: center;
    width: 100%;
    position: relative;
    color: white;

    img {
        margin-top: 10rem;
        z-index: -3;
        width: 100%;
        height: 450px;
        overflow: hidden;
        object-fit: cover;

    }
}

.wrapper {
    width: 600px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    h2 {
        margin-top: 12rem;
        font-size: 45px;
        font-weight: bold;
    }

    button:hover {
        background-color: #39FFBF;
        color: #1F1E38;
    }

    button {
        margin-top: 2rem;
        padding: 1.5rem 3rem;
        background-color: #1F1E38;
        color: white;
        border: none;

    }
}
</style>