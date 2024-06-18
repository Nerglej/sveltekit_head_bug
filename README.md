# svelte:head with components
There's a problem with how components are used in svelte:head.

To see this in action, run `npm run dev -- --open` and inspect the head element on the page with the debug tools in your browser. When navigating with the anchor between the two pages, existing titles and metatags keep exisiting, where it is expected to be removed to optimize e.g. SEO. Besides not updating the title in the browser since the browser uses the first instance of the title, it also just polutes the head element, which doesn't mean much in short visits, but in some extreme cases it could lead to a problem I guess.

See more in https://github.com/sveltejs/kit/issues/12365
