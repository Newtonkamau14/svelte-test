<script>
  export let showModal = false;
  export let isPromo = false;
</script>

{#if showModal}
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <div class="backdrop" class:promo={isPromo} on:click|self>
    <div class="modal">
        <slot name="title"></slot>
        <p>Hey there...</p>
        <slot></slot>
    </div>
  </div>
{/if}

<style>
  .backdrop {
    width: 100%;
    height: 100%;
    position: fixed;
    background: rgba(0, 0, 0, 0.8);
  }
  .modal {
    padding: 10px;
    border-radius: 10px;
    max-width: 400px;
    margin: 10% auto;
    text-align: center;
    background: white;
  }
  .promo .modal{
    background: crimson;
    color: white;
  }
</style>
