<script>
import Hero from '../Components/Hero.svelte'
import {link} from 'svelte-routing'
// featured products
import Featured from '../Components/Products/Featured.svelte'
</script>
<style>

</style>
<Hero>
<a href='/products' class='btn btn-primary btn-hero' use:link>Shop Now</a>
</Hero>
<Featured title='featured products'/>