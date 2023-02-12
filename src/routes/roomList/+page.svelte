<script>
	let rooms = [
		{
			roomName: 'QWERTY',
			roomID: '000000',
			roomDes: '선린 웹 동아리 쿼티의 공식 MitSub 방입니다.'
		},
		1,
		2,
		3,
		4,
		5,
		6,
		7,
		8
	];
</script>

<svelte:head>
	<link rel="stylesheet" href="src/css/roomList.css" />
</svelte:head>

<main>
	<div class="room-search mg-cen">
		<p class="p-bigxb mg-sml">방 찾기</p>
		<p class="p-smll mg-sml">숙제를 제출할 방을 찾아주세요</p>
		<input type="text" class="inp mg-sml" placeholder="방 이름 또는 아이디 검색" />
	</div>
	<ul class="room-list mg-cenX">
		{#each rooms as room, i}
			<li class="mg-big">
				<div class="room pd-sml">
					<div class="room-banner" />
					<div class="room-text pd-big">
						<a href="/roomList">
							<span class="p-bigb">{room.roomName}</span> <span class="p-smll">{room.roomID}</span>
						</a>
						<p class="p-smll">{room.roomDes}</p>
					</div>
				</div>
			</li>
		{/each}
	</ul>
</main>
