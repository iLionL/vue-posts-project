<template>
  <div class="post" >
    <div>
      <div><strong>ID : </strong>{{post.id}}</div>
      <div><strong>Title : </strong>{{post.title}}</div>
      <div><strong>Description : </strong>{{post.body}}</div>
    </div>
    <div class="post-button-del">
      <custom-button
      @click="$emit('remove', post)"
      >
        Delete
      </custom-button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
       required: true,
    }
  }
}
</script>

<style scoped>
.post {
  padding: 15px;
  border: 2px solid rgb(98, 0, 255);
  margin-top: 15px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.post-button-del{

}
</style>