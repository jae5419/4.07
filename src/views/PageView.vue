<template>
  <div>
    <h3>{{ obj.board[index].id }}페이지입니다</h3>
    <p>{{ obj.board[index].memo }}</p>
  </div>
</template>

<script>
import text from '../data.json'

export default {
  name: 'PageView',
  data() {
    return {
      obj: text
    }
  },
  computed: {
    index: function() {
      if(isNaN(this.$route.params.id))
      {
        return 0;
      }
      else
      {
        return this.$route.params.id-1;
      }
    }
  }
}
</script>
