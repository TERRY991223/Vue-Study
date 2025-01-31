<template >
    <div class="search-box">
        <input type="search" 
        @change="
        //검색창에 입력했을때 전달할 함수
        $emit('searchMovie', $event.target.value)
        inputText = $event.target.value;
        //검색창을 비워주는 것
        $event.target.value=''
        "
        placeholder="검색어">
        <button>검색</button>
    </div>
    <p>{{ inputText }}</p>
</template>
<script>
export default {
    name:"SerchBarComponent",
    data() {
        return{
            inputText: '',
        }
    },
    props:{
        data: Array,
    } ,   
    watch:{
        inputText(name){
            //입력한 영화제목이 데이터에 있는지 확인
            const findName=this.data.filter(movie => {
                return movie.title.includes(name);
            })
        if(findName.length == 0) {
            alert('해당하는 자료가 없습니다.')
        }
        }
    }
}
</script>
<style >
    .search-box{
        padding: 10px;
        display: flex;
        justify-content: center;
    }

    .search-bar input {
        padding: 5px 10px;
    }

    .search-box button {
        margin: 0;
    }
</style>