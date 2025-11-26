# CHT Technology Radar for Implementers
This is the repository of the [CHT Technology Radar for Implementers](https://docs.communityhealthtoolkit.org/cht-tech-radar-implementers/) content.

If you are looking for the content of the [CHT Technology Radar for Contributors](https://docs.communityhealthtoolkit.org/cht-tech-radar-contributors/), you can find it [in its dedicated GitHub repository](https://github.com/medic/cht-tech-radar-contributors). 

This Tech Radar is built by using the [CHT Technology Radar Core](https://github.com/medic/cht-tech-radar-core), which contains the skeleton app and the CHT look-and-feel styles. 

## Contribute to the Technical Radar

### Create a new Technology Radar release
For a new Technology Radar release, create a folder of the release date (YYYY-MM-DD) under `./radar`.

### Maintaining content
The items are written in Markdown (`.md`) format.

Each file has a meta header where the attributes of the item are listed:

```
---
title:      "CHT Sync"
ring:       adopt
quadrant:   methods-and-patterns
tags: [data, pipeline]
---

Text goes here. You can use **markdown** here.
```

Following front-matter attributes are possible:

- **title**: Name of the Item
- **quadrant**: Quadrant. One of `languages-and-frameworks` (for `App Building` quadrant),
  `methods-and-patterns` (for `Data Use` quadrant), `platforms-and-aoe-services`
(for `Deployment Management` quadrant), `tools` (for `CHT App Features` quadrant)
- **ring**: Ring section in radar. One of `trial`, `adopt`, `stop`
- **tags**: Optional tags for filtering.
- **featured**: (Optional, default "true") If you set this to "false", the item
  will not be visible in the radar quadrants but still be available in the overview.

The name of the .md file acts as item identifier and may overwrite items with
the same name from older releases.

If an item is overwritten in a new release, the attributes from the new item are
merged with the old ones, and a new history entry is created for that item.

You can integrate images in your markdown. Put the image files in your public folder and reference them:

```
![an image](/images/an-image.png)
```

### Content guidelines
You can update the rings and the quadrants in the `config.json` file. If you update the names of the rings and quadrants,
you will need to update the technologies .md files accordingly.

The text on the "How to use the CHT Technology Radar for Implementers" page can be updated in the `about.md` file.

### Customize the radar
> Further instructions on how to customize the Technical Radar can be found in the [medic/cht-tech-radar-core](https://github.com/medic/cht-tech-radar-core) repository.

## Development

### Host the application under a sub path
To host the application under a sub path, set the environment variable `PUBLIC_URL`, e.g. "/cht-tech-radar".
The default is `/`.

> For local development you can use `/build` and use this for the following steps. 

### Build the radar
Node.js >= 20 is required.

```
npm ci
npm run serve
```

Then open the Tech Radar here: http://localhost:3000/cht-tech-radar-implementers

### Build the radar with static files
```
npm ci
npm run build
```

> [!NOTE]
> The CHT Technology Radars are built starting from the [AOE Tech Radar content](https://www.aoe.com/techradar/index.html).
If you want to build your own Technical Radar you may want to have a look at the [AOE Tech Radar GitHub repository](https://github.com/AOEpeople/aoe_technology_radar).
