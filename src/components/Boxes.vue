<template>
    <div id="container-box">
        <div id="box-text">
            <h1>{{ title }}</h1>
            <p>{{ description }}</p>
        </div>
        <div id="box-img">
            <img :src="this.img">
        </div>
    </div>
</template>

<script>
export default {
    name: "boxesInfo",
    props: ["title","description","img"]
} 

</script>

<style scoped>
    #container-box {
        width: 100%;
        height: 100%;
        padding: 50px 260px;
        display: flex;
        flex-direction: row;
        background-color: black;
        border-bottom: 8px solid #222;
        justify-content: center;
        align-items: center;
    }

    #container-box:nth-child(1) {
        margin-top: -100px;
    }

    #container-box:nth-child(2),
    #container-box:nth-child(4) {
        flex-direction: row-reverse;
    }

    #container-box #box-text {
        display: flex;
        flex-direction: column;
        color: white;
    }

    #container-box #box-text:nth-child(1),
    #container-box #box-text:nth-child(3) {
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

    #container-box #box-img:nth-child(2),
    #container-box #box-img:nth-child(4) {
        padding-right: 60px;
    }

    @media screen and (max-width: 950px) {
        #container-box {
            display: flex;
            flex-direction: column;
            align-content: center;
            justify-content: center;
        }

        #container-box:nth-child(2),
        #container-box:nth-child(4) {
            flex-direction: column;
        }
  
        #container-box #box-text {
            align-items: center;
        }

        #container-box #box-text:nth-child(1),
        #container-box #box-text:nth-child(3) {
            padding-right: 0;
        }
        
        #container-box #box-text h1 {
            font-size: 2.1rem;
        }

        #container-box #box-text h1:nth-child(1) {
            text-align: center;
        }

        #container-box #box-text p {
            font-size: 1.2rem;
            text-align: center;
        }

        #container-box #box-img:nth-child(2),
        #container-box #box-img:nth-child(4) {
            padding-right: 0;
        }
    }
</style>