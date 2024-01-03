Steps to reproduce:

1. Clone repo
2. Cache deno deps
3. Run `netlify dev` and open the site
4. View the console for the error `ReferenceError: React is not defined`

Expected behavior:

We'd like to use JSX in our Netlify Edge Functions without needing to import React. To do this with Deno, we add it to the [Deno configuration file](https://docs.deno.com/runtime/manual/getting_started/configuration_file#compileroptions).

Running `netlify dev` should output `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"><div>Hello World</div>` in the console and the site should load without errors.

To see a working version, run `deno run index.tsx` and inspect the console output.

Versions:

deno: 1.39.1
netlify-cli: 17.11.0