<script>
import SpeciesSelect from "../lib/client/SpeciesSelect.svelte"

let species = ''
</script>
<article class="Column">
  <div style="text-align:center">
    <cyan-icon noun="ll" large/>
  </div>
  <h1 class="downscaled">Hahmokone</h1>
  <p>Epävirallinen L&L Hahmokone. Luo hahmon pelaajan kirjan antamassa järjestyksessä, ja täyttää lomakkeen valmiiksi.</p>
  <section class="fieldSet">
    <SpeciesSelect bind:species={species} />
    <p>[{species}]</p>
  </section>
</article>
