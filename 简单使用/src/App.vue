<template>
  <div id="app">
    <quill-editor
      id="quill-editor"
      v-model="content"
      :options="editorOption"
      @change="onEditorChange($event)"
    >
    </quill-editor>
  </div>
</template>

<script>
import QuillEditor from 'vue-quill-editor'

export default {
  name: 'App',
  data: function () {
    return {
      content: '',
      editorOption: {}
    }
  },
  methods: {
    onEditorChange() {
      console.log(this.content);
    }
  }
}
</script>

<style>
#app {
  width: 800px;
  height: 500px;
}

#quill-editor {
  width: 100%;
  height: 100%;
}
</style>