# comunica-web-client

A Web-based client to query the Web of Linked Data, using SPARQL or GraphQL-LD, powered by [Comunica](https://comunica.dev/).

This repo simply includes [@comunica/web-client-generator](https://github.com/comunica/jQuery-Widget.js/) as a dependency and calls it in a build script to generate a static site containing the web client.

A curated set of example queries is included in the [/queries](https://github.com/beeldengeluid/comunica-web-client/tree/main/queries) folder.

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

## Adding Datasources

In [`settings.json`](https://github.com/beeldengeluid/comunica-web-client/blob/main/settings.json), add to the datasources array:

```json
"datasources": [
  {
    "name": "NISV SPARQL",
    "url": "https://cat.apis.beeldengeluid.nl/sparql"
  }
]
```

## Adding Queries

In the [`/queries` directory](https://github.com/beeldengeluid/comunica-web-client/tree/main/queries), add a .sparql file containing:
- On the first line: '# ' + Title of the query to display in the dropdown
- On the second line: '# Datasource: ' + URL to the associated Datasource (if any)
- A valid SPARQL query

See for example [`children-of-program.sparql`](https://github.com/beeldengeluid/comunica-web-client/blob/main/queries/nisv/children-of-program.sparql).
