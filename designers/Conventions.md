## Naming Conventions

### File Naming

File naming should allow you to find your file among shambles, namely your "Open Recent" in your favorite design software.

I ultimately settled on this structure:
### `client_project_type`

For example, for our website, this would turn into `nextmoov_website_app`.

---

### Layer Naming

This can be a tough rule to follow, but it just requires a habit of doing so. 
Make it a habit to name your layer as soon as your drew it, so you won't forget it and won't have to come back later to it.

#### Artboards

Artboards must be named according to the screen you're currently designing.
Home screen should be named "Home", Settings screen is "Settings", and… well you got it.

In Framer X, content artboards sometimes need to be created in order to make scrolling possible, for example. In this case, use the parent's name and append ` - Content` to it.

#### Sketch Symbols / Framer X Components

Follow the same naming logic as from Artboards. Symbols need to be nested and easy to read.

#### Non-exported Layers

There isn't a specific naming rule for layers that do not need to be exported. Make them clear and understandable.

#### Exported Layers

Layers that need to be exported must follow a logical naming scheme depending on what it is you're exporting:

- icons, generally: `icon-[name].ext`
- icons variant (bitmap-only): `icon-[name]-[variant].ext`
- icons set: `[set]-[name].ext`
- illustrations: `img-[name].ext`
- illustrations specific to a part/screen: `[screen]-img-[name].ext`

For bitmap files that require multiple resolutions, do not forget to append your file name with `@2x`, before the extension, and change accordingly.

## Working Conventions

### Work Logic

We use two different interaction design tools: Sketch, by BohemianCoding, and Framer X, by Framer.
After thorough inspection, I concluded that the optimal workflow would be to first use Sketch to iterate fast and quickly, and then switch to Framer X for interaction and component splitting.
But that's still a WIP.

#### Sketch

Sketch is where you'll have the most creative freedom since it's more capable than Framer X in many aspects.
The way we work with Sketch here at nextmoov is simple:

1. Draw an artboard
2. Name it
3. Work on it
4. Iterate by duplicating your current artboard
5. Continue working on the OG artboard

Symbols are really encouraged to be used as early as possible. This will prevent you from doing all the same work multiple times.

#### Framer X

At the moment, I still don't really know where Framer X lands in our workflow. It's oriented a lot towards front-end programming and follows a DOM-like pattern for its layering.
It's currently slightly limited in what its visual capabilities are, unless you dive into some code components and do the CSS yourself, like multiple fills for example.

I think Framer X would be great as a step 2 in our design workflow: prototyping.
This means that we would do the complete visuals in Sketch, and once set, we would ease towards decomposing the interface in code/design components.
Doing so would prepare the way for our developers.

What still needs to be figured out is how could nextmoov create a common components library that would be imported in our Framer X folders but which wouldn't be hosted in the Framer (Private) Store.

### File Optimization

#### SVG

We mostly only use SVG files, here at nextmoov, unless a technical aspect doesn't allow us to do so.
These files should be optimized on export, automatically, but this still means your work should be clean.
To do so, Install [SVGO Compressor](https://github.com/BohemianCoding/svgo-compressor) for your Sketch install.
If you can't or aren't using Sketch, use [SVGOMG](https://jakearchibald.github.io/svgomg/) in your browser.

#### Bitmap

We love high resolution here. Pixels have been banned from my eyesight since Retina has been a thing.
But we can't always use 4096 × 2160 images, right?
That's when you gotta know your compression algorithms.

The general rule when using bitmap here at nextmoov is that, we use JPG for larger formats, and PNG for smaller sizes. There is no straight rule to that, but unless you're making an icon or something that needs to be very crisp, you should probably stick to JPG.

Illustrations are usually in PNG, and photography is JPG. Mostly.

Thousands of software and online tools are available for compression, but I can recommend you [Optimage](https://getoptimage.com) or [ImageOptim](https://imageoptim.com).

Avoid lossy compression unless you need to lower the file size tremendously. Google Lighthouse should warn our developers about any files being too large.
