# HTML Images, CSS Color & Text

## HTML Media

### Images in HTML

> - Use the `<img>` element to put a simple image on a webpage. This is an empty element (meaning that it has no text content or closing tag) that requires a minimum of one attribute to be useful — src (sometimes spoken as its full title, source). The src attribute contains a path pointing to the image you want to embed in the page, which can be a relative or absolute URL, in the same way as href attribute values in `<a>` elements. E.g. `<img src="dinosaur.jpg">`.
> - Elements like `<img>` and `<video>` are sometimes referred to as replaced elements because the element's content and size are defined by an external resource (like an image or video file), not by the contents of the element itself.
> - Alternative text with the `alt` attribute: Its value is supposed to be a textual description of the image, for use in situations where the image cannot be seen/displayed.
>   - Helpful if the user is visually impaired, and is using a screen reader to read the web out to them. In fact, having alt text available to describe images is useful to most users.
> - You can use the `width` and `height` attributes to specify the width and height of your image.
> - Add `title` attributes to images, to provide further supporting information if needed. But this is not recommeneded due to accessibility issues.
> - Annotate images with figures and figure captions using the HTML5 `<figure>` and `<figcaption>` elements. These are created for exactly this purpose: to provide a semantic container for figures, and to clearly link the figure to the caption
>   - A figure doesn't have to be an image.
> - Use CSS to embed images into webpages with the CSS `background-image` property, and the other `background-*` properties, are used to control background image placement.
> - ([from MDN docs](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML))

### Common Image Types

> | Abbreviation | File Format | MIME type | File ext. |
> | --- | --- | --- | --- |
> | APNG | Animated Portable Networks Graphics | image/apng | .apng |
> | AVIF | AV1 Image File Format | image/avif | .avif |
> | GIF | Graphics Interchange Format | image/gif | .gif |
> | JPEG | Joint Photo. Expert Group image | image/jpeg | .jpg, .jpeg, .jfif, .pjpeg, .pjp |
> | PNG | Poratable Network Graphics | image/png | .png |
> | SVG | Scalable Vector Graphics | image/svg+xml | .svg |
> | WebP | Web Picture foramt | image/webp | .webp |
> ([from MDN docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#common_image_file_types))

### Choosing an image format

> | Use | Best choice | Fallback choice | Note |
> | --- | --- | --- | --- |
> | Photograph | WebP or JPEG | JPEG | Photographs typically fare well with lossy compression. |
> | Icons | SVG, Lossless WebP, or PNG | PNG | use a lossless format to avoid loss of detail in a size-constrained image. |
> | Screenshots | Lossless WebP or PNG; JPEG if compression artifacts aren't a concern | PNG or JPEG; GIF for screenshots with low color counts | use a lossless format for screenshots to avoid compromising image quality under lossy compression |
> | Diagrams, drawings, and charts | SVG | PNG | SVG is the best choice for any image that can be represented using vector graphics |
> ([from MDN docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#choosing_an_image_format))

---

1. What is a real world use case for the `alt` attribute being used in a website? **The user is visually impaired and using a screen reader**
2. How can you improve accessibility of images in an HTML document? **Use captions (with the `<figure>` and `<figcaption>` HTML5 elements) and the `alt` text**
3. Provide an example of when the `figure` element would be useful in an HTML document. **The `figure` element is used to provide semantic container for figures, and to clearly link the figure to the caption.**
4. Describe the difference between a `gif` image and an `svg` image, pretend you are explaining to an elder in your community.
    **`gif` is ideal for simple images or animations**
    **`svg` is best used for objects that must be drawn accurately at different sizes**
5. What image type would you use to display a screenshot on your website and why? **Lossless WebP or PNG. Text easily becomes fuzzy and unclear under lossy compression.**

---

## Learn CSS

### Applying color to HTML elements using CSS

### Fundamental text and font styling

---

1. Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge.
2. Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character?
3. What should you consider when choosing fonts for an HTML document?
4. What do font-size, font-weight, and font-style do to HTML text elements?
5. Describe two ways you could add spacing around the characters displayed in an h1 element.

---