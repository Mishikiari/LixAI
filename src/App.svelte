<script>
	import SearchBar from './SearchBar.svelte';
	import Translation from './Translation.svelte';
  
	let isDarkMode = false;
  
  </script>
  
  <main class:dark={isDarkMode}>
	
	<SearchBar />
	<Translation />
  
  </main>
  
  <style>
	
  </style>
  