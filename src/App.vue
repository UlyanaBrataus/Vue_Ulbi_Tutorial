<template> 
<div>
<form>
<input type="text" placeholder="название поста">
</form> 
  <div class="post" v-for="post in posts">
  <div> <strong>Название: </strong>{{post.title}}</div>
   <div> <strong>Описание: </strong>{{post.body}}</div>
</div> 

</div>
</template>

<script> 

export default {
  data() {
    return {
     posts: [
       {id: 1, title: 'JavaScript 1', body: 'Описание поста 1'},
       {id: 2, title: 'JavaScript 2', body: 'Описание поста 2'},
       {id: 3, title: 'JavaScript 3', body: 'Описание поста 3'},
     ]
    }
  },
  methods: {
 
  }
}

</script>

<style> /* если <style scoped>, это значит, что стили будут применимы только к этому компоненту и не будут доступны извне, тут он не нужен, т.к. App это корневой компонент */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
}
</style>
