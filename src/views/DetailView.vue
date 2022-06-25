<template>
    <div class="result-box">
        <p class="title"> {{ $route.params.name }} 후보 득표성향 분석</p>
        <div class="table" v-for="age in ages" :key="age.name">
            <AgesRowsView 
                :name="age.name" 
                :percentage="age.percentage" 
                :className="age.className"/>
        </div>
    </div>
</template>
<script>
import AgesRowsView from '@/components/AgesRows.vue';

export default {
    components: {
        AgesRowsView
    },
    data() {
        return {
            ages: [
                {name: "10대", percentage: "5 (10%)", className: "bar-10"},
                {name: "20대", percentage: "5 (10%)", className: "bar-10"},
                {name: "30대", percentage: "5 (10%)", className: "bar-10"},
                {name: "40대", percentage: "5 (10%)", className: "bar-10"},
                {name: "50대", percentage: "5 (10%)", className: "bar-10"},
                {name: "60대", percentage: "5 (10%)", className: "bar-10"},
                {name: "70대", percentage: "5 (10%)", className: "bar-10"},
                {name: "80대", percentage: "5 (10%)", className: "bar-10"},
                {name: "90대", percentage: "10 (20%)", className: "bar-20"},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.result-box {
    width: 100%;
    border: solid 1px black;
    text-align: left;
    padding: 15px;
    .title {
        display: inline-block;
        margin: 15px;
        width: 400px;
    }
    .table {
    }
}
</style>
