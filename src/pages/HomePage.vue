<template lang="">
    <!--========JUMBOTRON SECTION=========-->
    <section>
        <div class="col jumbotron">
            <ImageSlider/>

            <div class="jumbotron-content">
                <h1>
                    You can plant a dream
                </h1>
            </div>
        </div>
    </section>

    <!--========COMPANY SERVICES SECTION=========-->

    <section>
        <CompanyService />
    </section>

    <!--========PLANTING SECTION=========-->

    <section class="planting-section wavy-section">
        <div class="row">
            <div class="col-lg-6 col-sm-12 planting-content">
                <h1>
                    Let's reforest the planet with you
                </h1>
                <div class="d-flex">
                    <img src="../assets/planting.png" href="">
                    <p>
                        We care about the life of the forest. We will plant 1 tree together every time you place an order over €30
                    </p>

                </div>
            </div>
            <div class="col-lg-6 col-sm-12 seeding-img">
                <div>
                    <img src="../assets/plating-tree.png" href="Planting tree image">
                </div>
            </div>
        </div>
    </section>


    <!--========PLANT'S ITEM SECTION=========-->

    <section>
        <PlantsItem />
    </section>


</template>

<script>
import ImageSlider from '../components/ImageSlider.vue';
import CompanyService from '../components/CompanyService.vue';
import PlantsItem from '../components/PlantsItem.vue';


export default {
    name: 'HomePage',
    components: {
        ImageSlider, 
        CompanyService,
        PlantsItem,
    },
};
</script>

<style lang="scss" scoped>


// ========JUMBOTRON SECTION========= //

section{
    width: 100%;

    div.jumbotron{
        position: relative;
        filter: grayscale(40%);


        div.jumbotron-content{
            position: absolute;
            // width: 650px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            color: white;

            h1{
                font-size: 5rem;
                letter-spacing: .125rem;
                text-shadow: #2d531e 1px 0 10px;
            }
        }
    }
}

// ========PLANTING SECTION========= //

section.planting-section{
    margin-top: 4rem;

    div.seeding-img{
        height: 630px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #2f2f2f;

        img{
            border-radius: 50%;
            border: 1px solid #ffff;
        }
    }

    div.planting-content{
        background-color: #2f2f2f;
        display: flex;
        flex-direction: column;
        justify-content: center;

        h1{
            font-size: 5rem;
            padding-left: 3rem;
            color: #ffff;
        }
        div.d-flex{
            align-items: center;

                img{
                    height: 200px;
                    width: 250px;
                }
                p{
                    color: white;
                }
            }
        }
}



</style>