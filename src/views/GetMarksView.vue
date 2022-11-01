<template>
    <div>
    <section class="p-5" id="learn">
        <div class="container">
            <div class="row align-items-center justify-content-between">
                <div class="col-md">
                    <img src="@/assets/form.jpg" class="img-fluid" alt="">
                </div>
                <div class="col-md p-5">
                    <Form></Form>
                    <a href="#" class="btn btn-dark mt-3" @click="gotoResult">Predict Results</a>
                </div>
            </div>
        </div>
    </section>
    <FAQ></FAQ>
    </div>
</template>

<script>
    import Form from '@/components/form.vue'
    import FAQ from '@/components/FAQ.vue'

    export default{
        components:{
            Form,
            FAQ
        },
        methods:{
            gotoResult(){
                this.$router.push('/result');
            }
        }
    }
</script>