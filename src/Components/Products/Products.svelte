<script>
  // import { onMount, onDestroy } from "svelte";
  import products from "../../stores/defaultProducts";
  import Product from "./Product.svelte";
  import Loading from "../Loading.svelte";
  export let title = "";

  // let localProducts = [];
  // let unsubscribe;

  // onMount(()=> {
  //   unsubscribe = products.subscribe(storeValue => {
  //     localProducts = storeValue;
  //   })
  // })

  // onDestroy(()=> {
  //   unsubscribe()
  // })

  // console.log(products)
  // console.log($products)
</script>

<section class="section">
  <h2 class="section-title">{title}</h2>
  <div class="products-center">
    {#each $products as product (product.id)}
      <Product {product} />
    {:else}
      <Loading />
    {/each}
  </div>

</section>
