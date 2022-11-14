<script>
  import { fade, scale } from "svelte/transition";
  import FeedbackItem from "./FeedbackItem.svelte";
  import { FeedbackStore } from "../stores"


</script>

{#each $FeedbackStore as fb (fb.id)}
  <div in:scale={{ duration: 1000 }} out:fade={{ duration: 500 }}>
    <FeedbackItem item={fb} />
  </div>
{/each}
