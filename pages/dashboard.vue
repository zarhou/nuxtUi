<script>
	export default {
		name: 'dashboard',
		created() {
			window.addEventListener("keypress", function() {
				if(event.key === '?') {
					document.getElementById("search").focus();
				}
			});
		}
	}
</script>


<template>

<div class="ctn bg-gray-100 min-h-screen flex">

<!-- side bar -->
	<div class="sidebar fixed inset-y-0 left-0 w-16 bg-white">
		
		<div class="h-16 flex items-center justify-center">
			<svg class="w-12 h-12 fill-current selected" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48">
				<path d="M8 20v14h6V20H8zm12 0v14h6V20h-6zM4 44h38v-6H4v6zm28-24v14h6V20h-6zM23 2L4 12v4h38v-4L23 2z"/>
			</svg>
		</div>

		<!-- icons -->
		<div class="h-full flex flex-col justify-center">
			<div class="-mt-24">

				<div class="flex justify-between items-center w-full pr-3">
					<svg class="fill-current selected" width="4" height="41" viewBox="0 0 4 41" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M0 0C2.20914 0 4 1.79086 4 4V37C4 39.2091 2.20914 41 0 41V0Z"/>
					</svg>
					<svg class="icons w-8 h-8 fill-current selected" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 27">
					  <path d="M21.333 3H20V.333h-2.667V3H6.667V.333H4V3H2.667A2.666 2.666 0 000 5.667v18.666A2.666 2.666 0 002.667 27h18.666A2.666 2.666 0 0024 24.333V5.667A2.666 2.666 0 0021.333 3zM12 7a3.999 3.999 0 110 8 3.999 3.999 0 110-8zm8 16H4v-1.333c0-2.667 5.333-4.134 8-4.134s8 1.467 8 4.134V23z"/>
					</svg>
				</div>

				<div class="mt-16 flex justify-between items-center w-full pr-3">
					<svg class="invisible" width="4" height="41" viewBox="0 0 4 41" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M0 0C2.20914 0 4 1.79086 4 4V37C4 39.2091 2.20914 41 0 41V0Z" fill="#0877F9"/>
					</svg>
					<svg class="icons w-8 h-8 fill-current unselected" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 26 24">
					  <path d="M24 20v1.333A2.666 2.666 0 0121.333 24H2.667A2.666 2.666 0 010 21.333V2.667A2.666 2.666 0 012.667 0h18.666A2.666 2.666 0 0124 2.667V4H12a2.666 2.666 0 00-2.667 2.667v10.666A2.666 2.666 0 0012 20h12zm-12-2.667h13.333V6.667H12v10.666zM17.333 14c-1.106 0-2-.893-2-2s.894-2 2-2c1.107 0 2 .893 2 2s-.893 2-2 2z"/>
					</svg>
				</div>

				<div class="mt-16 flex justify-between items-center w-full pr-3">
					<svg class="invisible" width="4" height="41" viewBox="0 0 4 41" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M0 0C2.20914 0 4 1.79086 4 4V37C4 39.2091 2.20914 41 0 41V0Z" fill="#0877F9"/>
					</svg>
					<svg class="icons w-8 h-8 fill-current unselected" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 28 28">
					  <path d="M12.667.667v26.666c-6.76-.673-12-6.386-12-13.333s5.24-12.667 12-13.333zm2.706 0V12.66h11.96C26.707 6.327 21.687 1.293 15.373.667zm0 14.673v11.993c6.314-.626 11.334-5.66 11.96-11.993h-11.96z"/>
					</svg>
				</div>

				<div class="mt-16 flex justify-between items-center w-full pr-3">
					<svg class="invisible" width="4" height="41" viewBox="0 0 4 41" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path d="M0 0C2.20914 0 4 1.79086 4 4V37C4 39.2091 2.20914 41 0 41V0Z" fill="#0877F9"/>
					</svg>
					<svg class="icons w-8 h-8 fill-current unselected" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 28">
					  <path d="M8 12.667H5.333v2.666H8v-2.666zm5.333 0h-2.666v2.666h2.666v-2.666zm5.334 0H16v2.666h2.667v-2.666zm2.666-9.334H20V.667h-2.667v2.666H6.667V.667H4v2.666H2.667C1.187 3.333.013 4.533.013 6L0 24.667a2.666 2.666 0 002.667 2.666h18.666c1.467 0 2.667-1.2 2.667-2.666V6c0-1.467-1.2-2.667-2.667-2.667zm0 21.334H2.667V10h18.666v14.667z"/>
					</svg>
				</div>

			</div>
		</div>
	</div>
<!-- // side bar -->

<!-- top bar -->
	<div class="fixed inset-x-0 top-0 ml-16 h-16 bg-red-300">
		<div class="topbar h-16 bg-white flex items-center justify-between">
			
			<div class="search-box relative ml-6 pl-4 flex items-center rounded-lg">
				<svg class="w-6 h-6 absolute" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M15.5 14H14.705L14.43 13.725C15.41 12.59 16 11.115 16 9.5C16 5.91 13.09 3 9.5 3C5.91 3 3 5.91 3 9.5C3 13.09 5.91 16 9.5 16C11.115 16 12.59 15.41 13.725 14.435L14 14.71V15.5L19 20.49L20.49 19L15.5 14ZM9.5 14C7.015 14 5 11.985 5 9.5C5 7.015 7.015 5 9.5 5C11.985 5 14 7.015 14 9.5C14 11.985 11.985 14 9.5 14Z" fill="#B6BECB"/>
				</svg>

				<input id="search" 
				class="input-search appearance-none bg-transparent text-gray-700 pl-8 pr-2 py-2 w-full" type="text" placeholder='Search  (Press "Shift + /" to focus)'>
			</div>

			<div class="h-full flex flex-row-reverse">
				<div class="h-full w-20 flex items-center justify-center border-l">
					<svg class="w-8 h-8" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 36 36">
					  <path d="M19.5 4.5h-3v15h3v-15zm7.245 3.255l-2.13 2.13A10.38 10.38 0 0128.5 18c0 5.805-4.695 10.5-10.5 10.5S7.5 23.805 7.5 18c0-3.285 1.515-6.21 3.87-8.13L9.255 7.755C6.345 10.23 4.5 13.89 4.5 18c0 7.455 6.045 13.5 13.5 13.5S31.5 25.455 31.5 18c0-4.11-1.845-7.77-4.755-10.245z" fill="#B6BECB"/>
					</svg>
				</div>
				<div class="h-full w-20 flex items-center justify-center border-l">
					<svg class="w-8 h-8 mt-1" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 36 36">
					  <path d="M20 1.333h-8V4h8V1.333zm-5.333 17.334h2.666v-8h-2.666v8zm10.706-8.814l1.894-1.893c-.574-.68-1.2-1.32-1.88-1.88l-1.894 1.893A11.949 11.949 0 0016 5.333c-6.627 0-12 5.374-12 12 0 6.627 5.36 12 12 12s12-5.373 12-12a11.95 11.95 0 00-2.627-7.48zM16 26.667a9.327 9.327 0 01-9.333-9.334A9.326 9.326 0 0116 8a9.326 9.326 0 019.333 9.333A9.327 9.327 0 0116 26.667z" fill="#B6BECB"/>
					</svg>
				</div>
				<div class="h-full flex items-center justify-center mr-12">
					<img class="w-12 h-12 rounded-full object-cover object-center" 
					src="https://images.unsplash.com/photo-1527980965255-d3b416303d12?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1400&q=80">
					<label class="text-gray-700 font-semibold inline-block -mt-1 ml-3">Ted Nguyen</label>
					<svg class="w-8 h-8" fill="none" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 36 36">
					   <path d="M9.333 13.333L16 20l6.667-6.667H9.333z" fill="#718096"/>
					</svg>
				</div>
			</div>

		</div>
	</div>
<!-- // top bar -->

<!-- content -->
	<div class="pl-16 pt-16 w-full">
		<div class="m-8 p-8 bg-white min-h-screen rounded-lg shadow-lg">
			<div class="flex justify-center items-center">
				<div class="grid grid-cols-3 col-gap-12">
					<div class="flex items-center justify-center">
						<span class="text-sm font-normal text-gray-700">3 Months</span>
					</div>
					<div class="flex items-center justify-center">
						<span class="text-lg font-semibold text-white bg-prm px-8 py-3 rounded-lg">6 Months</span>
					</div>
					<div class="flex items-center justify-center">
						<span class="text-sm font-normal text-gray-700">12 Months</span>
					</div>
				</div>
			</div>
			<div class="mt-12 grid grid-cols-3 gap-8">
				<div class="h-64 bg-gray-100 shadow-lg w-full rounded-lg" v-for="i in 100" :key="i"></div>
			</div>
		</div>
	</div>

</div>
	
</template>





<style lang="scss" scoped>

@import '@/assets/css/colors.scss';

// * {
// 	border-width: .1px;
// 	border-color: red;
// }

.topbar {
	box-shadow: 0rem .3rem .4rem #D0DCE7;
	clip-path: inset(0 0 -4rem 0); 

	.search-box {
		width: 100%;
		max-width: 40rem;
		transition: 150ms ease-in-out;
	}

	.search-box:focus-within {
		@apply bg-gray-100;
	}
}
.sidebar {
	box-shadow: .3rem 0rem .5rem #D0DCE7;

	.selected {
		color: $primary;
	}

	.unselected {
		color: $unselected-icon-color;
	}
}
</style>
