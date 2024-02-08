<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  export let xy = undefined;

  function selectUploadType() {
    dispatch("selected", {
      type: "audio",
      location: xy,
    });
  }
</script>
<div class="my-2">
<button class="phase1" on:click={selectUploadType}> record audio </button>
</div>
<style>
button {
  width: 100%;
}
</style>
