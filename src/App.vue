<template>
  <div id="app">
    <autocomplete :options="options" @select="onOptionSelect">
      <template slot="item" scope="option">
        <p>
          <strong>{{ option.first }} {{ option.second }}</strong>
        </p>
      </template>
    </autocomplete>
  </div>
</template>

<script>
import Autocomplete from './components/Autocomplete'

export default {
  name: 'app',
  components: {
    Autocomplete
  },
  data () {
    return {
      options: [{
        title: 'First Scene',
        description: 'test.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/1'
      }, {
        title: 'Second Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/2'
      }, {
        title: 'Third Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/3'
      }, {
        title: 'Fourth Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/4'
      }, {
        title: 'First Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/1'
      }, {
        title: 'Second Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/2'
      }, {
        title: 'Third Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/3'
      }, {
        title: 'Fourth Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/4'
      }, {
        title: 'First Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/1'
      }, {
        title: 'Second Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/2'
      }, {
        title: 'Third Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/3'
      }, {
        title: 'Fourth Scene',
        description: 'lorem ipsum dolor amet.',
        thumbnail: 'http://lorempicsum.com/nemo/200/200/4'
      }]
    }
  },
  methods: {
    onOptionSelect (option) {
      console.log('Selected option:', option)
    }
  }
}
</script>

<style>
  body {
    height: 100%;
  }
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    display: flex;
    justify-content: center;
    padding-top: 100px;
    height: 100%;
  }

  .control {
    width: 100%;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  input {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    width: 100%;
  }

  .autocomplete-input {
    width: 500px;
    position: relative;
    height: 300px;
  }

  ul.options-list {
    margin-top: -10px;
    border-radius: 0 0 3px 3px;
    position: absolute;
    width: 100%;
    text-align: left;
    border: none;
    border-top: none;
    max-height: 400px;
    overflow-y: auto;
    border: 1px solid #871A0B;
  }

  ul.options-list li {
    width: 100%;
    flex-wrap: wrap;
    background: white;
    margin: 0;
    border: 1px solid #871A0B;
    color: #363636;
    padding: 7px;
    cursor: pointer;
  }

  ul.options-list li.highlighted {
    background: #f8f8f8
  }
</style>
