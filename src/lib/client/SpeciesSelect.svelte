<script lang="ts">
import type { CyanSelect } from '@11thdeg/cyan'
	import { onMount } from 'svelte';

export let species = ''

let selectComponent: CyanSelect

onMount(() => {
  selectComponent.options = [
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
  selectComponent.value = species
})

function handleChange(event: Event) {
  if (!event.target) return
  species = (event.target as CyanSelect).value
}
</script>

<cyan-select bind:this={selectComponent} on:change={handleChange} />