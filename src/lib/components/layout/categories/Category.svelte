<script lang="ts">
	import Image from '$lib/components/ui/Image.svelte';

	const { name, slug, imgUrl } = $props();
	const imageUrl_220x220 = (imgUrl ?? '').replace('w_400,h_400', 'w_220,h_220');
</script>

<a href={`/categories/${slug}`} class="category-tile">
	<Image src={imageUrl_220x220} alt={name} className="image-container" />
	<h2 class="category-title">{name}</h2>
</a>

<style>
	.category-tile {
		display: block;
		text-decoration: none;
		color: #333;
		background-color: white;
		border-radius: 12px;
		overflow: hidden;
		box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
		transition: box-shadow 0.2s;
		text-align: center;
		border: 2px solid transparent;
		transition: border-color 0.3s ease;
		padding: 8px;
	}

	.category-tile:hover {
		border-color: var(--main-color);
		box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
	}

	.category-title {
		font-size: 1.4rem;
		padding: 8px 4px;
		margin: 0;
		color: var(--main-color);
	}
</style>
