<script>
  export let segment;
  let isOpen = false;
</script>

<style>
  @media (min-width: 769px) {
    nav {
      border-bottom: 1px solid gray;
    }
  }
</style>

<nav class="navbar">
  <div class="navbar-brand">
    <a href="/" class="navbar-item">
      <img src="logo.jpg" alt="covid" />
    </a>

    <a
      role="button"
      class="navbar-burger burger"
      class:is-active={isOpen}
      on:click={() => (isOpen = !isOpen)}
      aria-label="menu"
      aria-expanded="false">
      <span aria-hidden="true" />
      <span aria-hidden="true" />
      <span aria-hidden="true" />
    </a>
  </div>

  <div class="navbar-menu" class:is-active={isOpen}>
    <div class="navbar-start">
      <a href="/" class="navbar-item" class:is-active={segment === undefined}>
        Home
      </a>
      <a
        href="/about"
        class="navbar-item"
        class:is-active={segment === 'about'}>
        About
      </a>

    </div>
  </div>
</nav>
