<template>
<div class="min-h-screen">

	<div class="landing h-screen flex flex-col relative">

		<div class="background opacity-25 w-full fixed"></div>

		<nav class="navbar text-primary font-semibold px-4 py-4 w-full max-w-6xl mx-auto">
			<ul class="flex justify-end">
				<li class="ml-4 text-lg px-4 py-2">Home</li>
				<li class="ml-4 text-lg px-4 py-2">Shoes</li>
				<li class="ml-4 text-lg px-4 py-2">About</li>
				<li class="px-4 py-2 flex">
					<svg class="w-6 h-6 fill-current text-primary inline"  viewBox="0 -31 512.00026 512" xmlns="http://www.w3.org/2000/svg"><path d="m164.960938 300.003906h.023437c.019531 0 .039063-.003906.058594-.003906h271.957031c6.695312 0 12.582031-4.441406 14.421875-10.878906l60-210c1.292969-4.527344.386719-9.394532-2.445313-13.152344-2.835937-3.757812-7.269531-5.96875-11.976562-5.96875h-366.632812l-10.722657-48.253906c-1.527343-6.863282-7.613281-11.746094-14.644531-11.746094h-90c-8.285156 0-15 6.714844-15 15s6.714844 15 15 15h77.96875c1.898438 8.550781 51.3125 230.917969 54.15625 243.710938-15.941406 6.929687-27.125 22.824218-27.125 41.289062 0 24.8125 20.1875 45 45 45h272c8.285156 0 15-6.714844 15-15s-6.714844-15-15-15h-272c-8.269531 0-15-6.730469-15-15 0-8.257812 6.707031-14.976562 14.960938-14.996094zm312.152343-210.003906-51.429687 180h-248.652344l-40-180zm0 0"/><path d="m150 405c0 24.8125 20.1875 45 45 45s45-20.1875 45-45-20.1875-45-45-45-45 20.1875-45 45zm45-15c8.269531 0 15 6.730469 15 15s-6.730469 15-15 15-15-6.730469-15-15 6.730469-15 15-15zm0 0"/><path d="m362 405c0 24.8125 20.1875 45 45 45s45-20.1875 45-45-20.1875-45-45-45-45 20.1875-45 45zm45-15c8.269531 0 15 6.730469 15 15s-6.730469 15-15 15-15-6.730469-15-15 6.730469-15 15-15zm0 0"/></svg>
					<div class="ml-2 w-6 h-6 bg-primary rounded-full text-white text-center font-semibold">1</div>
				</li>
			</ul>
		</nav>

		<div class="inner-box px-4 flex-grow-1 flex items-center justify-between w-full max-w-6xl mx-auto">
			<div class="text-secondary">
				<h2 class="font-russo-one text-6xl">Run faster</h2>
				<p class="font-russo-one text-4xl leading-10 lead">made for heigh speed running </p>
				<div class="mt-24">
					<button class="font-russo-one px-6 py-2 text-lg rounded-sm bg-secondary text-white">Shop Now</button>
					<button class="font-russo-one px-6 py-2 text-lg ml-6 rounded-sm border-2 border-secondary text-primary">
						Learn More
					</button>
				</div>
			</div>
			<div>
				<img src="@/assets/img/shoes21.png">
			</div>
		</div>

	</div>

</div>
</template>

<style lang="scss" scoped>

@import url('https://fonts.googleapis.com/css?family=Russo+One&display=swap');

* {
	font-family: 'Roboto', sans-serif;
}

.background {
	background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='32' viewBox='0 0 16 32'%3E%3Cg fill='%239C92AC' fill-opacity='0.4'%3E%3Cpath fill-rule='evenodd' d='M0 24h4v2H0v-2zm0 4h6v2H0v-2zm0-8h2v2H0v-2zM0 0h4v2H0V0zm0 4h2v2H0V4zm16 20h-6v2h6v-2zm0 4H8v2h8v-2zm0-8h-4v2h4v-2zm0-20h-6v2h6V0zm0 4h-4v2h4V4zm-2 12h2v2h-2v-2zm0-8h2v2h-2V8zM2 8h10v2H2V8zm0 8h10v2H2v-2zm-2-4h14v2H0v-2zm4-8h6v2H4V4zm0 16h6v2H4v-2zM6 0h2v2H6V0zm0 24h2v2H6v-2z'/%3E%3C/g%3E%3C/svg%3E");
	z-index: -1;	
}

nav {
	font-family: Montserrat;
}

.landing {
	background-color: #D9D9D9;
	z-index: -10;
}

.text-primary {
	color: #636877;
}

.text-secondary {
	color: #813638;
}

.bg-primary {
	background-color: #636877;
}

.bg-secondary {
	background-color: #813638;
}

.border-secondary {
	border-color: #813638;
}

.font-main {
	font-family: '', 'sanserif';
}

.flex-grow-1 {
	flex-grow: 1;
}

.font-russo-one {
	font-family: 'Russo One', sans-serif;
}

</style>
