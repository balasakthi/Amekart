<template>
  <header>
    <nav
      class="navbar is-transparent is-fixed-top"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="container">
        <div class="navbar-brand">
          <NuxtLink class="navbar-item is-size-3 has-text-weight-bold" to="/"
            ><i class="fa-solid fa-bag-shopping mr-4"></i>Amekart</NuxtLink
          >
          <a
            role="button"
            class="navbar-burger"
            aria-label="menu"
            aria-expanded="false"
          >
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </a>
        </div>
        <div id="navbarExampleTransparentExample" class="navbar-menu">
          <div class="navbar-end">
            <NuxtLink class="navbar-item" to="/"> Home </NuxtLink>
            <NuxtLink class="navbar-item" to="/about"> About </NuxtLink>
            <div class="navbar-item">
              <div class="field is-grouped">
                <p class="control">
                  <NuxtLink class="button is-primary is-rounded" to="/products">
                    <span class="icon">
                      <i class="fa-solid fa-tag"></i>
                    </span>
                    <span>Products</span>
                  </NuxtLink>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </header>
  <main>
    <slot />
  </main>
</template>

<script>
export default {};
</script>

<style></style>
