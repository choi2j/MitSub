<script>
	let user = false;
	let src = 'src/img/logo.svg';
</script>

<svelte:head>
	<link rel="stylesheet" href="src/css/globals.css" />
	<link rel="stylesheet" href="src/css/header.css" />
</svelte:head>

<header class="pd-big">
	<img {src} alt="logo" class="img"/><p class="p-bigb"><span class="blue-color">Mit</span><span class="orng-color">Sub</span></p>
	<nav>
		<div class="pd-sml">
			<a href="/" class="whit-color p-smll">홈</a>
			{#if user == false}
				<a href="/login" class="whit-color p-smll">로그인</a>
				<a href="/register" class="whit-color p-smll">회원가입</a>
			{:else}
				<a href="/roomList" class="whit-color p-smll">방 검색</a>
				<a href="/user" class="whit-color p-smll">유저</a>
			{/if}
		</div>
	</nav>
</header>

<slot />

<style>
</style>
