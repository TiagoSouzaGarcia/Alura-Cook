<script>
  //Prop para definir a classe. Ele será usada dinamicamente.
  export let ativa = false;
  export let selecionavel = false;

  function aoClicar() {
    if (selecionavel) {
      ativa = !ativa;
    }
  }
</script>

<div class="tag" class:ativa on:click={aoClicar}>
  <slot />
</div>

<style>
  .tag {
    height: 48px;
    border-radius: 8px;
    padding: 1rem;
    text-align: center;
    color: var(--cor-texto-principal);
    background-color: var(--cinza);

    display: flex;
    justify-content: center;
    align-items: center;
  }

  .ativa {
    color: var(--branco);
    background-color: var(--laranja);
  }
</style>
