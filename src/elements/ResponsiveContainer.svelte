<script>
  export let tall = true;
  export let secondary = false;
</script>

<style>
  section {
    width: 100%;
  }

  .responsive {
    max-width: 968px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
  }
  .primary {
    background: #fffbd8;
  }

  .secondary {
    background: #fff172;
  }

  .short {
    height: auto;
  }

  @media only screen and (min-aspect-ratio: 1/1) {
    section {
      width: 100%;
      display: flex;
      flex-direction: row;
      justify-content: center;
    }

    .responsive {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      max-width: 968px;
    }
    .tall {
      height: 70vh;
    }

    .short {
      height: 30vh;
    }

    .primary {
      background: #fffbd8;
    }

    .secondary {
      background: #fff172;
    }
  }
</style>

<section class={secondary ? 'secondary ' : 'primary '}>
  <div class={'responsive ' + (tall ? 'tall ' : 'short ')}>
    <slot />
  </div>
</section>
