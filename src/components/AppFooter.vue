<script>
import { store } from "../store.js"
export default {
    name: "AppFooter",
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <section>
        <div class="flex-box">
            <div>
                <img src="public/logotype-2-150x25.png" alt="">
            </div>
            <div>
                <ul v-for="link in this.store.headerLinks">
                    <li>{{ link }}</li>
                </ul>
            </div>
            <div>
                <i class="fa-brands fa-instagram"></i>
                <i class="fa-brands fa-linkedin-in"></i>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
            </div>
        </div>

        <p class="terms">Terms of use</p>
        <div>
            <div class="info-wrapper">
                <p>Privacy Environmental Policy</p>
                <p>Copyright © 2023 Phlox Consulting. All Rights Reserved.</p>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.flex-box {
    width: calc(100% - 4rem);
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    padding: 4rem 0;
    color: white;
    border-bottom: 1px solid gray;



    ul {
        display: inline-block;
        list-style: none;
        margin: 0 0.8rem;
        color: grey;
    }

    i {
        margin: 0 0.8rem;
    }
}

.terms {
    margin-top: 2.5rem;
    padding-left: 2rem;
}

.info-wrapper {
    width: calc(100% - 4rem);
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
}

p {
    font-size: 16px;
    color: gray;
}

section {
    padding-bottom: 3rem;
}
</style>