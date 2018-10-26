<template>
    <div id="Calculadora">
        <div class="row">
            <div class="col-md-3">
            </div>
            <div class ="col-md-6">
                <form>
                    <div class="form-group">
                        <label for="numericos1">Numericos</label>
                        <input type="number" class="form-control" id="numericos1" v-model.number="numerico1" placeholder="Enter numericos">
                    </div>
                    <div class="form-group">
                        <label for="numericos2">Numericos 2</label>
                        <input type="number" class="form-control" id="numericos2" v-model.number="numerico2" placeholder="Enter numericos 2">
                    </div>
                    <div class="form-group">
                        <div class="row">
                            <div class="col-md-3">
                                <button type="button" class="btn btn-secondary btn-block" @click="sum">+</button>
                            </div>
                            <div class="col-md-3">
                                <button type="button" class="btn btn-secondary btn-block" @click="min">-</button>
                            </div>
                            <div class="col-md-3">
                                <button type="button" class="btn btn-secondary btn-block" @click="prod">*</button>
                            </div>
                            <div class="col-md-3">
                                <button type="button" class="btn btn-secondary btn-block" @click="div">/</button>
                            </div>
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="exampleFormControlTextarea1">Numericos res</label>
                        <textarea class="form-control" v-model.number="result" id="exampleFormControlTextarea1" rows="3" disabled></textarea>
                    </div>
                </form>
            </div>
                <div class="col-md-3">
            </div>
        </div>
    </div>
</template>

<script>
    import Store from '../store'
    export default {
        name: "Calculadora",
        data() {
            return {
                numerico1: 0,
                numerico2: 0,
                result:  Store.state.result
            }
        },
        methods: {
            sum() {
                this.result = this.numerico1 + this.numerico2;
                Store.state.result = this.result;
            },
            min() {
                this.result = this.numerico1 - this.numerico2;
                Store.state.result = this.result;
            },
            prod() {
                this.result = this.numerico1 * this.numerico2;
                Store.state.result = this.result;
            },
            div() {
                this.result = this.numerico1 / this.numerico2;
                Store.state.result = this.result;
            }
        }
    }
</script>

<style scoped>

</style>