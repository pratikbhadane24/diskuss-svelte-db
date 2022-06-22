<script>
  import Diss from "./Diss.svelte";
  import DissStore from "../stores/DissStore";
  import { onMount, onDestroy } from "svelte";

  let allDiss;
  let dissStoreUnsub = DissStore.subscribe((data) => (allDisss = data));

  onMount(() => {
    console.log("Component Mounted");
  });
  onDestroy(() => {
    dissStoreUnsub();
  });
</script>

<div class="all-chits">
  {#each allDiss as diss (diss.id)}
    <Diss {...diss} />
  {/each}
</div>
