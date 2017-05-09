<template>
    <div class="row">
    <br>
        <div class="col-sm-8 col-sn-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <label>Quote</label>
        <textarea name="form-control" class="form-control"  rows="6" v-model="quote"></textarea>
        </div>
             <div class="col-sm-8 col-sn-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
            <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
        </div>
    </div>
</template>

<script>
    export default {
        data: () => {
            return {
                quote: ''
            };
        },
        methods: {
            createNew() {
                this.$emit('quoteAdded', this.quote);
                 this.quote  = '';
            }
        }

    }
</script>

<style>
</style>