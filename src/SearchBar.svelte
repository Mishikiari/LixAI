<script>
	let searchTerm = '';
	let isDarkMode = false;
  
	function search() {
	  console.log('Ricerca:', searchTerm);
	}
  
	function toggleTheme() {
	  isDarkMode = !isDarkMode;
	  document.body.classList.toggle('dark');
	}
  </script>
  
  <main class:dark={isDarkMode}>
	<h1>LixAI</h1>
	<input type="text" bind:value={searchTerm} placeholder="Inserisci l'URL, il magnet o seleziona un file" />
	<button on:click={search}>Translate</button>
  
	<div class="theme-toggle">
	  <label>
		<input type="checkbox" bind:checked={isDarkMode} />
		<span>{isDarkMode ? 'Light Theme' : 'Dark Theme'}</span>
	  </label>
	</div>
  </main>
  
  <style>
	main {
	  max-width: 400px;
	  margin: 0 auto;
	  padding: 2rem;
	  text-align: center;
	  border-radius: 8px;
	  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
	  transition: background-color 0.3s ease;
	}
  
	h1 {
	  font-size: 24px;
	  margin-bottom: 1rem;
	}
  
	input,
	button {
	  margin-top: 1rem;
	  padding: 8px 12px;
	  font-size: 16px;
	  border-radius: 4px;
	  border: 1px solid #ccc;
	  width: 100%;
	}
  
	button {
	  background-color: #007bff;
	  color: #fff;
	  cursor: pointer;
	}
  
	.theme-toggle {
	  position: fixed;
	  bottom: 20px;
	  right: 20px;
	}
  
	.theme-toggle label {
	  display: flex;
	  align-items: center;
	  color: #000;
	}
  
	.theme-toggle input {
	  margin-right: 8px;
	}
  
	.theme-toggle span {
	  color: #000;
	  margin-left: 4px;
	}
  
	.dark {
	  background-color: #333;
	  color: #fff;
	}
  
	.dark input,
	.dark button {
	  background-color: #555;
	  color: #fff;
	}
  
	body.dark {
	  background-color: #111;
	  color: #fff;
	}
  </style>
  