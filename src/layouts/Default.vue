<template>
  <div class="layout">
    <header data-v-7e33895e="" class="header">
      <div data-v-7e33895e="" class="container">
        <div data-v-7e33895e="" class="left">
          <a
            data-v-7e33895e=""
            href="/"
            aria-current="page"
            class="home-link active--exact active"
            ><img
              data-v-7e33895e=""
              src=".././assets/img/logo.332701b7.svg"
              alt="Nichlas W. Andersen"
              class="logo"
          /></a>
        </div>
        <nav
          data-v-7e33895e=""
          class="nav right"
          _msthash="520860"
          _msttexthash="22478794"
        >
          <a
            data-v-7e33895e=""
            href="/journal"
            class="nav__link"
            _istranslated="1"
            >Journal</a
          ><a
            data-v-7e33895e=""
            href="/contact"
            class="nav__link"
            _istranslated="1"
            >Say Hi!</a
          >
        </nav>
      </div>
    </header>

    <slot />

    <footer data-v-07acb5f8="" class="footer">
      <div data-v-07acb5f8="" class="container">
        <span data-v-07acb5f8="" _msthash="339276" _msttexthash="16871504"
          >Copyright © 2021</span
        >
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
@import '.././assets/css/main.css';
</style>
