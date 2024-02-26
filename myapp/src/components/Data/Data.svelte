<script>

let name = "Svelte";
  let src = "https://giphy.com/embed/duzpaTbCUy9Vu";

</script>

<h1>Hello {name.toLocaleLowerCase()}</h1>

<img {src} alt="A man dances." />

<!--This is a dynamic attribute -->

<iframe
  {src}
  width="480"
  height="433"
  frameBorder="0"
  class="giphy-embed"
  title="Name"
  allowFullScreen
></iframe>

<!--This is a dynamic attribute with the same name -->

<iframe
  {src}
  width="480"
  height="433"
  frameBorder="0"
  class="giphy-embed"
  title="Name"
  allowFullScreen
></iframe>

<!-- You can add your style  -->

<style>


  /** With this tag you can applie style over other components*/
  /* :global(h1) {
    color: goldenrod;
    font-family: "Comic Sans MS", cursive;
    font-size: 2em;
    text-align: center;
    animation: zoom 5s;
  } */

  @keyframes zoom {
    0%,
    100% {
      transform: scale(3);
    }
    50% { transform: scale(0.5)}
  }
</style>