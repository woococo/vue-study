<template>
    <div class="result-box">
        <h3 class="title">* 후보별 득표율</h3>
        <p className="name">이름</p> <p className="rate">인기도</p>
        <div class="table" v-for="candi in candidates" :key="candi.name">
            <CandidatesRowsView 
                :name="candi.name" 
                :percentage="candi.percentage" 
                :className="candi.className"
                :info="candidates" />
        </div>
    </div>
</template>
<script>
import CandidatesRowsView from '@/components/CandidatesRows.vue';

export default {
    components: {
        CandidatesRowsView
    },
    data() {
        return {
            candidates: [
                {name: "1번 가연", percentage: "425(12%)", className: "bar-12"},
                {name: "2번 나연", percentage: "859(24%)", className: "bar-24"},
                {name: "3번 다연", percentage: "898(25%)", className: "bar-25"},
                {name: "4번 라연", percentage: "900(25%)", className: "bar-25"},
                {name: "5번 마연", percentage: "436(12%)", className: "bar-12"},
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.result-box {
    width: 100%;
    border: solid 0px black;
    text-align: left;
    padding: 15px;
    .title {
        display: inline-block;
        // margin: 15px;
        width: 200px;
    }    
}

.name {
    margin: 0 0 0 0;
    width: 100px;
    padding: 5px 0px 5px 0px;
    border: solid 1px black;
    text-align: center;
    .text {
        display: block;
        margin-top: 9px;  
    }
}

.rate {
    padding: 5px 0px 5px 0px;
    position: absolute;
    top:126px;
    left:125px;
    text-align:center;
    width: 480px;
    border: solid 1px black;
}


</style>
