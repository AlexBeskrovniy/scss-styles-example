<script lang="ts">
    import UserCard from './UserCard.svelte';
    import ProductCard from './ProductCard.svelte';
</script>

<style lang="scss">
  @import 'mixins';
  $textColor: #A79EA4;
  .main {
      height: 100vh;
      color: $textColor;
      @include flex-center();
    }
</style>

<main class="main">
  <!-- <UserCard /> -->
  <ProductCard />
</main>
