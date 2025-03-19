<script lang="ts">
	import { page } from '$app/state';
</script>
<header>
	<div class="navbar bg-base-100 shadow-sm">
		<div class="flex-1">
			<h4 aria-current={page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Programowanie w Piskorzowie</a>
			</h4>
		</div>
		<div class="flex-none">
			<ul class="menu menu-horizontal px-1">
				<li aria-current={page.url.pathname === '/' ? 'page' : undefined}>
					<a href="/">Home</a>
				</li>
				<li>
					<details>
						<summary>Parent</summary>
						<ul class="bg-base-100 rounded-t-none p-2">
							<li><a>Link 1</a></li>
							<li><a>Link 2</a></li>
						</ul>
					</details>
				</li>
			</ul>
		</div>
	</div>
</header>


<style>
	header {
		z-index: 10;
	}
</style>
