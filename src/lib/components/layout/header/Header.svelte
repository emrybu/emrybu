<script lang="ts">
	import logo from '$lib/assets/logo.svg';
	import Menu from '../menu/Menu.svelte';
	import MenuButton from '../menu/MenuButton.svelte';

	let isMenuOpen = $state(false);

	function closeMenu() {
		isMenuOpen = false;
	}

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}
</script>

<div class="header-block">
	<div class="header-content">
		<div class="left-part">
			<div class="header-logo">
				<a href="/">
					<img src={logo} alt="EMRYBU" />
				</a>
			</div>
			<div class="menu-block">
				<MenuButton {isMenuOpen} {toggleMenu} />
				<Menu {isMenuOpen} close={closeMenu} />
			</div>
		</div>
	</div>
</div>

<style>
	.header-block {
		width: 100%;
		height: 56px;
		position: sticky;
		top: 0;
		z-index: 100;
		box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
		background-color: rgba(var(--main-color-rgb), 0.1);
	}

	.header-content {
		max-width: 1366px;
		margin: 0px auto;
		padding: 0px 12px;
		height: 100%;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 4px;
	}

	.left-part {
		display: flex;
		align-items: center;
	}

	.header-logo {
		width: 120px;
		height: 40px;
	}

	.menu-block {
		margin-left: 12px;
		position: relative;
		flex-shrink: 0;
	}
</style>
