<!-- components/macropad/MacropadView.svelte  -->

<script>
	import Module from "./Module.svelte";

  export let modules;  // Receive module prop from parent

</script>

<style lang="css">
  .macropad-view {
    display: grid;
    gap: 5px;
    padding: 10px;
    margin: 0 auto;
    position: relative;
    border-radius: 10px;
  }

  .module-container {
    display: flex;
    align-items: center;
    justify-content: center;
    /* border: 1px solid #ccc; */
    /* background-color: #fff; */
    padding: 10px;
    border-radius: 5px;
    font-size: 14px;
    text-align: center;
  }
</style>


<div class="macropad-view">
  {#each modules as moduleInfo}
    <div class="module-container">
      <Module {moduleInfo}/>
    </div>
  {/each}
</div>