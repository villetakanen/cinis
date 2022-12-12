<script lang="ts">
import '@11thdeg/cyan/style.css'
import '@11thdeg/cyan'
</script>

<cyan-navigation-rail>
  <cyan-navigation-button noun="page" active/>
  <cyan-spacer />
  <cyan-navigation-button noun="fox" label="Pelilauta" />
  <cyan-navigation-button noun="avatar" label="Kirjaudu" />
</cyan-navigation-rail>

<main class="bookLayout appContent">
  <slot></slot>
</main>