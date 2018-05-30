# PreloadedImg

Small React Component used for preloading img elements. Used and created by @ntslive.

On component render, the component will display an img tag rendering the `thumbnailUrl` image and make a request for the `imageUrl` image. Once the `imageUrl` image has been downloaded by the browser, the component will rerender the component using this image.

## Installation

Include as dependency in `package.json`:

`"preloaded-img": "github:ntslive/preloaded-img#0.1.0"`

Note that this requires the Git tag `0.1.0` to be present.

Then run `npm install` as usual.

## Usage

```
const PreloadedImg = require('PreloadedImg');

const IndexPage = (
    <div>
        <PreloadedImg
            thumbnailUrl="https://media2.ntslive.co.uk/resize/200x200/a7e5f382-8605-4eb3-8eeb-e604b6ca674a_1457395200.jpeg"
            imageUrl="https://media2.ntslive.co.uk/resize/1600x1600/a7e5f382-8605-4eb3-8eeb-e604b6ca674a_1457395200.jpeg"
            description="Andrew Weatherall Show Image"
        />
    </div>
)
```

### Required Properties:

* `thumbnailUrl` the URL of the thumbnail image to be used initially within the `img` element. Roughly 200x200 sized images are recommended.
* `imageUrl` The URL of the final image to be used within the `img` element.

### Optional Properties:

* `description` The text to be used within the alt tag of the `img` element.

## Viewing a sample

Run `npm run sample` to create the required javascript bundle.

View the working example by opening `sample.html` directly in the browser.

## Updating the package

Run `npm run setup` to create a require pre-commit hook for the repository. This builds a babel'd `index.js` file in the `build` folder.