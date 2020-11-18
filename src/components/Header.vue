<template>
    <header class="container d-flex bd-navbar">
        <div class="text-light w-100  text-center title-navbar">{{title}}</div>
    </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
      title: String
  }
}
</script>

<style>
.bd-navbar {
        min-height: 4rem;
        background-color: var(--bg-official);
        box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, .05), inset 0 -1px 0 rgba(0, 0, 0, .1);
        padding-top: .5em;
        padding-bottom: .5em;
        border-top-left-radius: 16px;
        border-top-right-radius: 16px;
}
    
.title-navbar {
    font-family: var(--font-body);
    font-weight: 600;
    font-size: 35px;
}
</style>