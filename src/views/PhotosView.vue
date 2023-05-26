<template>
    <div>
        <div class="home">
            <router-link to="/">
                <i class="fa-sharp fa-solid fa-angles-left"></i>
                <p>Main page</p>
            </router-link>
        </div>
        <h1 class="title-photos">Photos</h1>

        <div class="close">
            <i class="fas fa-xmark"></i>
        </div>
        <div class="main-images">

            <div class="image">
                <img class="img"  v-for="photo in photos" :key="photo" :src="photo" alt="">
                <div class="back-shadow" v-show="backshaddow">
                </div>
            </div>
        </div>

    </div>
</template>

<script>

export default {
    data() {
        return {
            photos: [
                
            ],
            backshaddow: false,


        }
    },
    mounted() {
        const photo = document.querySelectorAll("img");
        const close = document.querySelector(".close");
        const body = document.querySelector("body");

        close.style.display = "none";
        photo.forEach(photos => {
            photos.addEventListener("click", () => {
                photos.classList.add("active");
                body.style.overflow = "hidden";
                this.backshaddow = true;

                close.style.display = "flex";
                close.addEventListener("click", () => {

                    this.backshaddow = false;
                    photos.classList.remove("active");
                    close.style.display = "none";
                    body.style.overflow = "visible";
                })
            })
        })

    }

}

</script>

<style lang="scss" scoped>
.close {
    position: fixed;
    top: 20px;
    right: 20px;
    width: 30px;
    height: 30px;
    font-size: 20px !important;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    border-radius: 5px;
    z-index: 5 !important;
    background: #eee;
}
.back-shadow{
    position: fixed;
    top: 0;
    left: 0;
    background: #00000077;
    backdrop-filter: blur(5px) saturate(100%);
    height: 100vh;
    width: 100%;
    z-index: 3;
}

.main-images {
    max-width: 800px;
    margin: 0 auto;
    margin-top: 5rem;
    padding: 2rem 2rem 5rem 2rem;



    .image {
        position: relative;
        display: grid;
        gap: 1.5rem;
        grid-template-columns: 1fr 1fr 1fr 1fr;

        .active {
            position: fixed !important;
            height: auto !important;
            width: 400px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 4;
            transition: 0s ease;
        }
        .active:hover{
            opacity: 1;
        }


        img {
            padding: 0.3rem;
            background: #eeeeee7b;
            border-radius: 5px;
            width: 150px;
            height: 150px;
            margin: 0 auto;
            object-fit: cover;
            cursor: pointer;
        }

        img:hover {
            opacity: 0.9;
        }
    }
}





.home a {
    position: fixed;
    bottom: 0;
    z-index: 2;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 5px;
    font-size: 14px !important;
    text-decoration: none;
    width: 100%;
    padding: 5px 0;
    text-align: center;
    background: #eeeeee45;
    backdrop-filter: blur(10px) saturate(200%);
    color: #fff;

    i {
        margin-right: 2px;
        margin-top: 0.5px;
        transition: .4s;
        font-size: 10px;
    }
}

.home a:hover i {
    margin-right: 10px;
}

.title-photos {
    margin-top: 10rem;
    color: #eeeeee45;
    font-size: 4rem;
    text-align: center;
}
</style>