<template>
  <div class="home">
    <ul class="argitu-menu-wrapper">
      <li class="argitu-menu-wrapper__item">
        <a class="argitu-menu-item">
          <div class="argitu-menu-item__label">Home</div>
        </a>
      </li>
      <li class="argitu-menu-wrapper__item">
        <a class="argitu-menu-item">
          <div class="argitu-menu-item__label">Galería</div>
        </a>
      </li>
      <li class="argitu-menu-wrapper__item">
        <a class="argitu-menu-item">
          <div class="argitu-menu-item__label">Experiencias</div>
        </a>
      </li>
      <li class="argitu-menu-wrapper__item">
        <a class="argitu-menu-item">
          <div class="argitu-menu-item__label">Blog</div>
        </a>
      </li>
      <li class="argitu-menu-wrapper__item">
        <a class="argitu-menu-item">
          <div class="argitu-menu-item__label">Contacto</div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='scss' scoped>
.argitu-menu-wrapper {
  padding: 0px;
  display: flex;
}

.argitu-menu-wrapper__item {
  display: flex;
  flex-grow: 1;
  flex-basis: 0;

  &:not(:first-child) {
    margin-left: 4px;
  }

  &:not(.is-inactive) {
    transition: background-color 0.3s;

    &:hover,
    &.is-hover {
      cursor: pointer;
      background-color: #c4c4b0;
    }
  }

  &:hover .argitu-menu-item__label {
    color: purple !important;
  }

  &.is-active {
    background-color: #c4c4b0;
    .argitu-menu-item__label {
      color: purple;
    }
  }
}

.argitu-menu-item {
  display: block;
  flex: 1;

  padding: 8px 0;

  border: 1px solid grey;
  border-radius: 3px;
  text-align: center;
}

.argitu-menu-item__label {
  padding: 2px;

  color: grey;
  font-weight: bold!important;
  text-transform: uppercase;
  font-size: 16px;
}
</style>
