## What is this?

Experimenting with serving Kaltura streams with the AblePlayer player.

[More Details](https://docs.google.com/document/d/1han1awbukgrNy_2-D0Y6m0R2qmGSytTfBZdBq14hSQs/edit)

## How do we do this?

See able-player-start.html, which is pretty much hacking around:

* fetch the MP4
* fetch the M3U8 playlist to get the subtitle playlist
* modify the subtitle URL to get the entire VTT in one fetch
* configure `<video>` element
* invoke AblePlayer on that element

**Is there a saner way?** [Maybe we can use kWidget?](http://player.kaltura.com/docs/index.php?path=getSources) (this gives you all the `<source>` but none of the caption `<track>`s)

## How to use this repository

Use `able-player-start.html` as a starting point --- it sets up the environment for AblePlayer and its dependencies. This includes jQuery if that has appeal.

We're working with `node v16` which can be installed with [nvm](https://github.com/nvm-sh/nvm/blob/master/README.md). If you have `nvm` installed, you can do `nvm use` once you're in this repository.

After your first checkout, do `npm install`.

To view examples: `npx http-server -p 5555` and then the examples will be available at https://localhost:5555/examples/

## Resources

[AblePlayer](https://github.com/ableplayer/ableplayer)

[Fulcrum Example](https://www.fulcrum.org/concern/file_sets/pk02cc67p?locale=en)

[Kaltura API v3](https://www.kaltura.com/api_v3/testmeDoc/)

[Kaltura API Authentication](https://developer.kaltura.com/api-docs/VPaaS-API-Getting-Started/Kaltura_API_Authentication_and_Security.html)

[Kaltura playManifest](https://developer.kaltura.com/api-docs/Deliver-and-Distribute-Media/playManifest-streaming-api.html)

