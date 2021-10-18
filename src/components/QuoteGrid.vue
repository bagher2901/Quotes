<template>
    <div class="row">
        <app-quote v-for="(item,index)  in quotes" @click.native="deleteQuote(index)">{{
            item
            }}
        </app-quote>


    </div>
</template>

<script>
    import Quote from "./Quote";

    export default {
        name: "QuoteGrid",
        props: ['quotes'],
        components: {
            appQuote: Quote,

        },
        methods:{
          deleteQuote(index){
              this.$emit('quoteDeleted',index)

          }
        }
    }
</script>

<style scoped>

</style>