<template>
  <nav class="border fixed split-nav">
    <div class="nav-brand">
      <h3>
        <a href="#">
          Paper Doc
        </a>
      </h3>
    </div>
    <div class="collapsible">
      <input
        id="collapsible1"
        type="checkbox"
        name="collapsible1"
      >
      <button>
        <label for="collapsible1">
          <div class="bar1" />
          <div class="bar2" />
          <div class="bar3" />
        </label>
      </button>
      <div class="collapsible-body">
        <ul class="inline">
          <li>
            <a href="#">
              Start
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'TheNavBar',
}
</script>

