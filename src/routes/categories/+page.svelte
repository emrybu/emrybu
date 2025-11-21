<script lang="ts">
	import Categories from '$lib/components/layout/categories/Categories.svelte';
	import { getCategories } from '$lib/store/appStore.svelte';
	const categories = getCategories();
</script>

<div class="categories-block">
	<h1>Наша продукція</h1>
	{#if categories.length > 0}
		<Categories {categories} />
	{:else}
		<p>Наразі категорії продукції відсутні.</p>
	{/if}
</div>

<style>
	.categories-block {
		max-width: 1200px;
		margin: 40px auto;
		padding: 20px;
	}

	h1 {
		text-align: center;
		margin: 20px 0px;
		color: var(--main-color);
	}
</style>
