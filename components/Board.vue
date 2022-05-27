<template>
  <div id="board">
    <div class="container">
      <b-jumbotron header="자유게시판" lead="학업에 필요한 정보들을 서로 묻고 답하세요." class="text-dark text-center my-5"></b-jumbotron>
      <b-table striped hover :items="items" :fields="fields" @row-clicked="rowClick"></b-table>
      <div class="text-center"><b-button @click="writeContent" class="mt-5 text-center bg-success">글쓰기</b-button></div>
    </div>
  </div>
</template>

<script>
import data from "@/data";

 
   let items = data.Content.sort((a, b) => {
      return b.content_id - a.content_id;
    }); // 내림차순
    const user_name='운영자'
  
export default {
  name: "Board",
  data() {
   
     return {
    
      // bootstrap 'b-table' 필드 설정
      fields: [
        {
          key: "content_id",
          label: "번호"
        },
        {
          key: "title",
          label: "제목"
        },
        {
          key: "user_name",
          label: "글쓴이"
        },
        {
          key: "created_at",
          label: "작성일"
        }
      ],
      items: items
    };
  },
  methods: {
  
    rowClick(items) {
      this.$router.push({
        path: `/detail/${items.content_id}`
      });
      
    },
   
    writeContent() {
      this.$router.push({
        path: `/create`
      });
      
    }
  },
  computed: {
    rows() {
        return this.items;
    }
  },
   
}
</script>
