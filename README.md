# AEM Editorial Toolbar - example configuration package

This is the example configuration package for the [AEM Editorial Toolbar](https://chromewebstore.google.com/detail/aem-editorial-toolbar/dadkbhhjkoakmjjgbmfccbadkdcjciie) browser extension.
It is a working package you can import as-is to see what one looks like, and a starting point to fork and point at your own AEM estate.

The hostnames in `environment-config.yaml` are placeholders such as `author.yourcompany.com`.
The package imports cleanly, but it will not do anything useful until you replace them with your own hosts.

## Try it

[Install the extension](https://chromewebstore.google.com/detail/aem-editorial-toolbar/dadkbhhjkoakmjjgbmfccbadkdcjciie) from the Chrome Web Store, then open this URL in Chrome:

https://raw.githubusercontent.com/tomgibson/aem-editorial-toolbar-example-config/main/examplecompany.aem-toolbar.json

The extension recognises the manifest and offers to import the package.
The four YAML files sit alongside the manifest at the same URL prefix, so the relative paths in it resolve without any further setup.

## Make it yours

1. Fork this repository, or just copy the five files.
2. Put your own author and public hostnames in `environment-config.yaml`. That is the only file most teams need to change.
3. Host the folder anywhere your team's browsers can reach it over HTTPS, with no interactive login in front of the files. An intranet server, a cloud bucket, GitHub Pages and raw GitHub all work.
4. Send your own manifest URL to your team. Each person opens it and presses Import.

Keep the `.aem-toolbar.json` suffix when you rename the manifest.
That suffix is what makes the extension offer to import it.

## The files

| File | What it is |
|---|---|
| `examplecompany.aem-toolbar.json` | The manifest. Names the package and points at the four config files |
| `environment-config.yaml` | Your AEM author hosts, your public site domains, and how URLs map between them |
| `link-matrix.yaml` | Which quick links appear on each screen |
| `message-matrix.yaml` | Contextual warnings and tips |
| `region-map.yaml` | How the toolbar tells one AEM screen from another |

Each file is commented, so reading them top to bottom is a reasonable way to understand the options.

## Reference

The extension is on the [Chrome Web Store](https://chromewebstore.google.com/detail/aem-editorial-toolbar/dadkbhhjkoakmjjgbmfccbadkdcjciie).
The full configuration reference lives on the [documentation site](https://symphonious-narwhal-a4f248.netlify.app), which is not repeated here.
