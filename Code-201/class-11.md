# Audio, Video, Images

## Video and Audio Content

[Video and Audio Content](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)

---

1. Explain how the ability to use video and audio on the web has evolved since the early 2000s. **Early a/v on the web Flash, Silverlight, etc plug-ins that are now obsolete.**
2. Describe the use of the `src` and `controls` attributes in the `<video>` element.
    1. `src`: **The source attribute contains a path to the video you want to embed. It works in exactly the same way as with the `<img>` tag.**
    2. `controls`: **The controls attribute is used to to include the browser's own control interface, otherwise a developer would be required to build their interface using the appropriate JavaScript API.**
3. Why is it important to have fallback content inside the `<video>` element? **This is needed for older browsers that don't support the `<video>` element. This provides a fall back option to display something in lieu of the missing video.**
4. Write a very short story where `<audio>` and `<video>` are characters. **There was once a audio who was friends with a video. One day, he challenged the video to a race. Seeing how slow the video was going, the audio thought he’ll win this easily. So he took a nap while the video kept on going. When the audio woke up, he saw that the video was already at the finish line. Much to his chagrin, the video won the race while he was busy sleeping. [Video killed the audio star](https://www.youtube.com/watch?v=W8r-tXRLazs&ab_channel=TheBugglesVEVO).**

---

## A Complete Guide to Grid

[A Complete Guide To Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

---

1. How does Grid layout differ from Flex? **Grid is made for two-dimensional layout while Flexbox is for one. This means Flexbox can work on either row or columns at a time, but Grids can work on both.** [GeeksForGeeks](https://www.geeksforgeeks.org/comparison-between-css-grid-css-flexbox/#:~:text=Grid%20is%20made%20for%20two,in%20this%20type%20of%20scenario.)
2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.
    1. Grid container: **The element on which display: grid is applied. It’s the direct parent of all the grid items.**
    2. Grid item: **The children (i.e. direct descendants) of the grid container.**
    3. Grid line: **The dividing lines that make up the structure of the grid. They can be either vertical (“column grid lines”) or horizontal (“row grid lines”) and reside on either side of a row or column.**

---

## Responsive Images

[Responsive Images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

---

1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive? **Having responsive images is important because it helps us deliver optimal file size, the right image for the right screen size, improves user experience and improves loading time.** [lab21](https://www.lab21.gr/blog/use-responsive-images/)
2. Define the following `<img>` attributes `srcset` and `sizes`. Write an example of how they are used.
    1. **`srcset` defines the set of images we will allow the browser to choose between, and what size each image is.**
    2. **`sizes` defines a set of media conditions (e.g. screen widths) and indicates what image size would be best to choose, when certain media conditions are true**

    ``` html
    <img srcset="elva-fairy-480w.jpg 480w,
             elva-fairy-800w.jpg 800w"
     sizes="(max-width: 600px) 480px,
            800px"
     src="elva-fairy-800w.jpg"
     alt="Elva dressed as a fairy">
     ```

3. How is `srcset` more helpful for responsive images than CSS or JavaScript? **The `<img srcset="" src="" alt="">` syntax is for serving differently-sized versions of the same image. You could try to serve entirely different images using this syntax, but browsers assume that everything in a srcset is visually-identical and will choose whichever size they think is best. Otherwise when the browser starts to load a page, it starts to download (preload) any images before the main parser has started to load and interpret the page's CSS and JavaScript.**

---

## For Further Review

- [Images in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML) - this is a review from Class 05
- [Other Embedding Technologies](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies)
