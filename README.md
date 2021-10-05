# comunica-web-client

A Web-based client to query the Web of Linked Data, using SPARQL or GraphQL-LD, powered by [Comunica](https://comunica.dev/).

This repo simply includes [@comunica/web-client-generator](https://github.com/comunica/jQuery-Widget.js/) as a dependency and calls it in a build script to generate a static site containing the web client.

A curated set of data sources and example queries is forthcoming.

## Local usage

install dependency:
```
npm install
```

generate the web client
```
npm run build
```

serve the generated web client in the `build` directory using your tool of choice, e.g. [serve](https://github.com/vercel/serve), [python 3's http.server](https://docs.python.org/3.8/library/http.server.html#http.server.SimpleHTTPRequestHandler):
```
serve ./build/
python -m http.server -d ./build/
```
