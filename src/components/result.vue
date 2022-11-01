<template>
    <div>
        <section class="p-5" id="learn">
            <h2 class="text-center mb-5">Predicted Colleges</h2>
            <!-- <img src="image" alt=""> -->
            <div class="container" v-for="detail in details">
                <div class="row align-items-center justify-content-between">
                    <div class="col-md">
                        <img v-bind:src="detail.img" class="img-fluid" alt="" style="height:250px;margin-left:50px">
                    </div>
                    <div class="col-md p-5">
                        <h2>{{detail.name}}</h2>
                        <p class="lead">
                            {{detail.location}}
                        </p>
                        <p class="lead">
                            {{detail.naac}}
                        </p>
                        <p class="lead">
                            {{detail.placement}}
                        </p>
                        <a href="#" class="btn btn-dark mt-3"><i class="bi bi-chevron-right"></i>Read More</a>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
    import kongu from "@/assets/kongu.jpeg";
    import vit from "@/assets/vit.jpg";
    import annauni from "@/assets/annauni.jpeg";

    export default{
        data(){
            return{
                img1:'kongu.jpeg',
                selected:-1,
                details:[
                    {
                    id:0,
                    name : 'Kongu Engineering College',
                    location : 'Perundurai, Erode, TamilNadu ',
                    naac : 'It has recieved NAAC accrediation of A+++ in the year 2022',
                    placement : 'Last year 200 companies visted the campus and 100% placement was shown for the year 2021-2022',
                    img:kongu
                    },//'Kongu Engineering College','Vellore Institute of Technolgy','Anna University'],
                    {
                    id:1,
                    name : 'Vellore Institute of Technolgy',
                    location : 'Vellore, TamilNadu ',
                    naac : 'It has recieved NAAC accrediation of A++ in the year 2022',
                    placement : 'Last year 100 companies visted the campus and 80% placement was shown for the year 2021-2022',
                    img:vit
                    },
                    {
                    id:2,
                    name : 'Anna University',
                    location : 'Chennai, TamilNadu ',
                    naac : 'It has recieved NAAC accrediation of A+in the year 2022',
                    placement : 'Last year 250 companies visted the campus and 97% placement was shown for the year 2021-2022',
                    img:annauni
                    }
            ]
            }
        },
        computed:{
                image(){
                    this.selected++;
                    return this.details[this.selected].img;
                }
        },
        created(){
            console.log(this.details[0].img);
        }
    }
</script>