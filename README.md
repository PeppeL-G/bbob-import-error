# Reproducible Instructions
1. `git clone https://github.com/PeppeL-G/bbob-import-error.git`
2. `cd bbob-import-error.git`
3. `npm install`
4. `npm run dev`
5. Open [http://localhost:5173/](http://localhost:5173/) in a web browser
6. Get the following error in the terminal:
	```
	TypeError: __vite_ssr_import_2__.default is not a function
			at /Users/peter/projects/bbob-import-error/src/routes/+page.svelte:9:38
			at Object.$$render (/Users/peter/projects/bbob-import-error/node_modules/svelte/src/runtime/internal/ssr.js:156:16)
			at Object.default (/Users/peter/projects/bbob-import-error/.svelte-kit/generated/root.svelte:45:41)
			at /Users/peter/projects/bbob-import-error/node_modules/@sveltejs/kit/src/runtime/components/layout.svelte:5:41
			at Object.$$render (/Users/peter/projects/bbob-import-error/node_modules/svelte/src/runtime/internal/ssr.js:156:16)
			at /Users/peter/projects/bbob-import-error/.svelte-kit/generated/root.svelte:44:40
			at $$render (/Users/peter/projects/bbob-import-error/node_modules/svelte/src/runtime/internal/ssr.js:156:16)
			at Object.render (/Users/peter/projects/bbob-import-error/node_modules/svelte/src/runtime/internal/ssr.js:164:17)
			at Module.render_response (/Users/peter/projects/bbob-import-error/node_modules/@sveltejs/kit/src/runtime/server/page/render.js:171:29)
			at async Module.render_page (/Users/peter/projects/bbob-import-error/node_modules/@sveltejs/kit/src/runtime/server/page/index.js:286:10)
	```
7. The code giving the error is the file [/src/routes/+page.svelte](./src/routes/+page.svelte):
	```html
	<script>
		
		import bbobHTML from '@bbob/html'
		import presetHTML5 from '@bbob/preset-html5'
		
	</script>
	
	<div>
		{bbobHTML(`[i]Text[/i]`, presetHTML5())}
	</div>
	```