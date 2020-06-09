<script>
  export let src = "/img/discord.png";
  export let text = "Discord";

  export let click = () => {
    console.log("Clicked");
  };
</script>

<style>
  button {
    box-sizing: border-box;
    background: none;
    padding: 8px;
    border: 2px solid black;
    border-right: 2px solid black;
    border-bottom: 2px solid black;
    transition: 0.1s all ease-in-out;
    width: 10rem;
    margin: 0.5rem 1rem 0.5rem 0;
    min-height: 4rem;
  }

  button:hover {
    padding: 8px;
    padding-left: 6px;
    padding-top: 6px;
    border: 2px solid black;
    border-right: 5px solid black;
    border-bottom: 5px solid black;
    background: #ffffff20;
  }

  button:active {
    padding: 8px;
    padding-left: 6px;
    padding-bottom: 6px;
    border: 2px solid black;
    border-left: 5px solid black;
    border-top: 5px solid black;
    background: #00000020;
    box-shadow: 1px 1px 3px #00000040;
  }

  h3 {
    white-space: nowrap;
  }
</style>

<button on:click={click} class="flex items-center justify-start">
  <div class="w-25 h-75">
    <img {src} alt={text} />
  </div>
  <div class="w-75">
    <h3 class="ma0 ph3">{text}</h3>
  </div>
</button>
