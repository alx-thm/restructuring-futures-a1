<script>
    import { onMount } from 'svelte';
    let tooltipDiv;
    export let text = '';
    let showTooltip = false;
    
    let position = { top: 0, left: 0 };
    
    onMount(() => {
      tooltipDiv.addEventListener('mouseover', () => { showTooltip = true; });
      tooltipDiv.addEventListener('mouseout', () => { showTooltip = false; });
    });
  </script>
  
  <div bind:this={tooltipDiv} class="tooltip">
    {#if showTooltip}
      <div class="tooltiptext">{text}</div>
    {/if}
    <slot></slot>
  </div>