<template>
    <div class="table-row">
        <div class="name">
            <router-link class="text" :to="{ name: 'detail', params: { name: name }}">{{ name }}</router-link>
        </div>
        <div class="rate">
            <img :class="className" src="@/assets/bar.png" />
            {{ percentage }}
        </div>
    </div>
</template>
<script>
export default {
    props: {
        name: String,
        percentage: String,
        className: String
    },
    data() {
        return {
        }
    },
}
</script>
<style lang="scss" scoped>
    .table-row {
        width: 600px;
        display: flex;
        flex-direction: row;
        .name {
            width: 100px;
            border: solid 1px black;
            text-align: center;
            .text {
              display: block;
              margin-top: 9px;  
            }
        }
        .rate {
            width: 480px;
            border: solid 1px black;
            padding-top: 10px;
            padding-bottom: 5px;
            .bar-12 {
                height: 20px;
                width: 60px;
            }
            .bar-24 {
                height: 20px;
                width: 120px;
            }
            .bar-25 {
                height: 20px;
                width: 125px;
            }
        }
    }

    
</style>