<template>
  <div id="app">
    <Topbar/>
    <main>
      <Editor class="editor" />
      <Preview class="preview" />
    </main>

  </div>
</template>

<script>

  import Topbar from './components/Topbar'
  import Editor from './components/Editor'
  import Preview from './components/Preview'
  import store from './store/index.js'
  export default {
    name: 'App',
    store,
    components: {
      Topbar, Editor, Preview,
    }
  }
</script>

<style lang="scss">
  *{margin: 0;padding: 0;box-sizing: border-box;}
  ul,li{
    list-style: none;
  }
  .icon {
    width: 1em;
    height: 1em;
    vertical-align: -0.15em;
    fill: currentColor;
    overflow: hidden;
  }

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    
    height: 100vh;
    display: flex;
    flex-direction: column;
  }

  main {
    display: flex;
    flex: 1;

    >.editor {
      min-width: 25em;
      margin: 16px 0 16px 16px;
      .tabs ol{
        margin-left: 3em;
        margin-top: 4em;
      }
    }
    >.preview {
      flex: 1;
      margin: 16px;
    }
  }
</style>