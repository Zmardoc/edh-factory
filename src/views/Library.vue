<template>
  <div class="library">
    <h2>Library</h2>
    <cardFilter />
  </div>
</template>

<script>
import cardFilter from "../components/cardFilter";
export default {
  name: "Library",
  components: {
    cardFilter
  }
};
</script>
