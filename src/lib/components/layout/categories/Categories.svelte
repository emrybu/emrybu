<script lang="ts">
	import Category from './Category.svelte';

	const { categories } = $props();
</script>

<div class="category-grid">
	{#each categories as category (category.slug)}
		<Category {...category} />
	{/each}
</div>

<style>
	.category-grid {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
		gap: 25px;
		margin-top: 30px;
	}
</style>
