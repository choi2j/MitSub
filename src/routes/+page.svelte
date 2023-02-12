<script>
	import Icon from 'svelte-awesome';
	import {
		search,
		download,
		upload,
		gears,
		lock,
		github,
		instagram,
		envelopeSquare,
		users
	} from 'svelte-awesome/icons';

	let user = true;
	let src = 'src/img/banner.svg';
</script>

<svelte:head>
	<link rel="stylesheet" href="src/css/home.css" />
</svelte:head>

<main>
	<div class="top">
		<div class="top-text">
			<p class="p-bigxl">
				<span class="orng-color p-bigxb">Submit</span> your
				<span class="blue-color p-bigxb">Work</span><br />
				오직 당신의 <span class="orng-color p-bigxb">과제</span>를 위한
				<span class="blue-color p-bigxb">서비스</span>
			</p>
		</div>
		<div class="top-img">
			<img {src} alt="banner-img" />
		</div>
	</div>
	<div class="bot">
		<div class="bot-buttons">
			{#if user == false}
                <a href="/login" class="a-big blue-back mg-sml">방 생성하기</a>
                <a href="/register" class="a-big orng-back mg-sml">방 참가하기</a>
			{:else}
			    <a href="/roomMake" class="a-big blue-back mg-sml">방 생성하기</a>
			    <a href="/roomList" class="a-big orng-back mg-sml">방 참가하기</a>
			{/if}
		</div>
		<div class="bot-contact">
			<p class="p-bigl">Contact</p>
			<div class="bot-contact-buttons">
				<a href="/" class="mg-sml"><Icon data={github} scale={3} /></a>
				<a href="/" class="mg-sml"><Icon data={instagram} scale={3} /></a>
				<a href="/" class="mg-sml"><Icon data={envelopeSquare} scale={3} /></a>
			</div>
		</div>
	</div>
</main>
