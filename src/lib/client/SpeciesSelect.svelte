<script lang="ts">
import type { CyanSelect } from '@11thdeg/cyan'

export let species = ''

let speciesOptions = [
  { value: '-', label: "- Valitse -"},
  { value: "elf", label: "Haltija" },
  { value: "human", label: "Ihminen" },
  { value: "dwarf", label: "Kääpiö" },
  { value: "dragonling", label: "Louhelainen" },
  { value: "gnome", label: "Maahinen" },
  { value: "halfling", label: "Puolituinen"},
  { value: "changeling", label: 'Vaihdokas'},
  { value: "orc", label: 'Örkki'}
]

function handleChange(event: Event) {
  if (!event.target) return
  species = (event.target as CyanSelect).value
}
</script>

<cyan-select value={species} label="Laji" options={speciesOptions} on:change={handleChange}/>