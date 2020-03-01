<template>
    <section class="container-fluid">

        <header class="row">
            <h1 id="configuration" class="configuration col-10 text-left">
                <span id="carModel" class="carModel">{{carModel}}</span>
                <span id="carEquipment" class="carEquipment">{{carEquipment}}</span>
                <span id="bodyType" class="bodyType">- {{bodyType}}</span>
            </h1>
            <button class="col-2" name="selectEquipment" id="selectEquipment">
                <span>{{selectName}}</span>
                <i class="fas fa-chevron-down"></i>
<!--                <i class="fas fa-chevron-up"></i>-->
            </button>
        </header>

        <div id="allEquipment" class="row">
            <article v-for="car in carEquipments" :key="car.equipment" class="optionEquipment col-3 ">
                <img :src="car.photo" :alt="car.photo">
                <h4>
                    <span>{{car.model}}</span>
                    <span>{{car.equipment}}</span>
                    <span>{{car.bodyType}}</span>
                </h4>
                <div class="body">
                    <a href="#">
<!--                        <svg class="bi bi-chevron-right" width="32" height="32" viewBox="0 0 20 20" fill="currentColor" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6.646 3.646a.5.5 0 01.708 0l6 6a.5.5 0 010 .708l-6 6a.5.5 0 01-.708-.708L12.293 10 6.646 4.354a.5.5 0 010-.708z" clip-rule="evenodd"/></svg>-->
                        <i class="fas fa-exchange-alt"></i>
                        <span>Сравнить</span>
                    </a>
                </div>
            </article>
        </div>

    </section>

</template>

<script>
    export default {
        name: "configurator",

        data() {
            return {
                carModel: "Camry",
                carEquipment: "Comfort",
                bodyType: "Седан бизнес класса",
                selectName: "Все комплектации",
                carEquipments: [
                    {
                        model:"Camry",
                        equipment: "Comfort",
                        bodyType: "Седан бизнес класса",
                        photo: "https://t1-resize.toyota-europe.com/ccis/zip/ua/product-token/e460cecd-1792-4c02-8749-96bc28a572ae/vehicle/97b1f1c6-0aab-4963-a46c-01bc214d6781/width/500/height/192/padding/0,0,0,40/image-quality/70/day-exterior-4_1f7.png"
                    },
                    {
                        model:"Camry",
                        equipment: "Elegance",
                        bodyType: "Седан бизнес класса",
                        photo: "https://t1-resize.toyota-europe.com/ccis/zip/ua/product-token/e460cecd-1792-4c02-8749-96bc28a572ae/vehicle/97b1f1c6-0aab-4963-a46c-01bc214d6781/width/500/height/192/padding/0,0,0,40/image-quality/70/day-exterior-4_1f7.png"
                    },
                ],
            }
        }


    }
    </script>

<style scoped>
    section {
        height: 298px;
        padding: 40px 44px 0 74px;
        font-size: 1.5rem;
        width: 100%;
    }

    header {
        padding-top: 100px;
        width: 100%;
        color: #202020;
        font-size: 1.5rem;
    }

    header .configuration {
        display: inline-block;
        font-size: 4.4rem;
        line-height: 4.4rem
    }

    header .configuration span {
        margin-right: 10px;
    }

    header .configuration .carModel {
        font-weight: 700;
    }

    header .configuration .bodyType {
        font-size: 2.2rem;
    }
</style>