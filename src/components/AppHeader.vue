<script>
import { store } from "../store.js"

export default {
    name: "AppHeader",
    data() {
        return {
            store
        }
    },

}
</script>

<template>
    <section>
        <div>
            <img src="/logotype.png" alt="">
        </div>
        <div>
            <ul>
                <li class="border">HOME</li>
                <li>ABOUT</li>
                <li>PROJECTS</li>
                <li>SERVICES</li>
                <li>BLOG</li>
                <li>CONTACT</li>
            </ul>
        </div>
    </section>
</template>



<style scoped lang="scss">
li {
    display: inline-block;
    margin: 0 1rem;
    font-weight: lighter;
    color: rgb(189, 189, 189);
    padding-top: 26px;
}


li:hover {
    border-top: 5px solid white;
    color: white;
    cursor: pointer;
}



.border {
    padding-top: 26px;
    border-top: 5px solid white;
    transform-origin: 0% 50%;
    color: white;
}

li:hover:after {
    transform: scaleX(1)
}

li:after {
    border-top: 5px solid white;

    transform-origin: 0% 50%
}

section {
    width: 100%;
    height: 50px;
    padding: 0 2rem;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
}

img {
    width: 110px;
}
</style>
