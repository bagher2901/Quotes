<template>
    <div class="row">
        <form>
            <div class="col-xs-12 col-md-6 col-md-offset-3 col-sm-8 col-sm-offset-2 form-group">
                <label>Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col-xs-12 col-md-6 col-md-offset-3 col-sm-8 col-sm-offset-2 form-group">
                <button class="btn btn-primary" @click.prevent="createNew">add Quote</button>
            </div>
        </form>


    </div>
</template>

<script>


    export default {
        name: "NewQuote",
        data() {
            return{
                quote:'',
            }

        },
        methods:{
            createNew(){
                this.$emit('quoteadded',this.quote);
                this.quote = ''
            }

        }



    }
</script>

<style scoped>

</style>