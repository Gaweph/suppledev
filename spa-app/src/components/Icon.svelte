<svg
  aria-hidden="true"
  class="{classes}"
  role="img"
  xmlns="http://www.w3.org/2000/svg"
  viewBox="{viewBox}"
>
  <path fill="currentColor" d="{path}" />
</svg>
<script>
  // import { IconDefinition } from "@fortawesome/free-solid-svg-icons";
  export let icon;
  export let large;

  let path = [];
  let classes = "";
  let viewBox = "";

  $: viewBox = "0 0 " + icon.icon[0] + " " + icon.icon[1];

  $: classes = "fa-svelte" + ($$props.class ? ' ' + $$props.class : "");

  $: path = icon.icon[4];
</script>

<style>
  .fa-svelte {
    width: 1em;
    height: 1em;
    overflow: visible;
    display: inline-block;
  }

  .fa-svelte.large {
    width: 1.5em;
    height: 1.5em;
  }
</style>