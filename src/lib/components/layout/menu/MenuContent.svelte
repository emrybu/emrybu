<script lang="ts">
	const { close } = $props();
</script>

<div class="menu-content">
	<nav class="nav-list">
		<a href="/orders" class="nav-link" onclick={close}>Мої замовлення</a>
		<div class="nav-separator"></div>
		<a href="/customer" class="nav-link" onclick={close}>Мої дані</a>
	</nav>
</div>

<style>
	.nav-separator {
		border-bottom: 2px solid var(--common-border);
	}

	.nav-list {
		display: flex;
		flex-direction: column;
		gap: 5px;
	}

	.nav-link {
		display: block;
		padding: 10px 15px;
		text-decoration: none;
		color: var(--common-text-dark, #495057);
		font-size: 1.2rem;
		border-radius: 4px;
		transition:
			background-color 0.2s,
			color 0.2s;
	}

	.nav-link:hover {
		background-color: var(--common-bg-hover, #e9ecef);
		color: #000;
	}
</style>
