<template>
    <div id="container-box">
        <div id="box-text">
            <h1>{{ title }}</h1>
            <p>{{ description }}</p>
        </div>
        <div id="box-img">
            <img src="/image/tv.png">
        </div>
    </div>
</template>

<script>
export default {
    name: "boxesInfo",
    props: ["img","alt","title","description"]
}
</script>

<style scoped>
    #container-box {
        width: 100%;
        height: 100%;
        padding: 50px 70px;
        display: flex;
        flex-direction: row;
        background-color: black;
        margin-top: -100px;
        border-bottom: 8px solid #222;
        justify-content: center;
        align-items: center;
    }

    #container-box #box-text {
        display: flex;
        flex-direction: column;
        color: white;
        padding-right: 60px;
    }

    #container-box #box-text h1 {
        font-size: 3.3rem;
    }

    #container-box #box-text p {
        margin-top: 30px;
        font-size: 1.6rem;
    }

    #container-box #box-img img {
        width: 530px;
    }

    @media screen and (max-width: 950px) {
        #container-box {
            display: flex;
            flex-direction: column;
            align-content: center;
            justify-content: center;
        }

        #container-box #box-text {
            align-items: center;
            
        }

        #container-box #box-text h1 {
            font-size: 2.1rem;
        }

        #container-box #box-text p {
            font-size: 1.2rem;
            text-align: center;
        }

    }
</style>