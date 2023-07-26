# React 3

## Reading

### [NextJs](https://nextjs.org/learn/basics/getting-started) (Through `Assets, Metadata, and CSS` section.)

- Next.js: The React Framework
  - An intuitive page-based routing system (with support for dynamic routes)
  - Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
  - Automatic code splitting for faster page loads
  - Client-side routing with optimized prefetching
  - Built-in CSS and Sass support, and support for any CSS-in-JS library
  - Development environment with Fast Refresh support
  - API routes to build API endpoints with Serverless Functions
  - Fully extendable
- Create a Next.js app
  - setup
    - `npx create-next-app@latest nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/learn-starter"`
    - this uses the tool called create-next-app, which bootstraps a Next.js app for you. It uses this template through the --example flag.
  - Run the development server
    - `npm run dev`
    - This starts your Next.js app’s "development server" (more on this later) on port 3000
  - The Next.js development server has Fast Refresh enabled. When you make changes to files, Next.js automatically applies the changes in the browser almost instantly.
- Navigate Between Pages
  - In Next.js, a page is a React Component exported from a file in the `pages` directory.
    - Pages are associated with a route based on their file name.
      - `pages/index.js` is associated with the / route.
      - `pages/posts/first-post.js` is associated with the /posts/first-post route.
    - The component can have any name, but you must export it as a default export.
  - In Next.js, you can use the `Link` Component `next/link` to link between pages in your application. `<Link>` allows you to do client-side navigation and accepts props that give you better control over the navigation behavior.
    - import the `Link` component from `next/link`
    - the `Link` component is similar to using `<a>` tags, but instead of `<a href="…">`, you use `<Link href="…">`
  - The `Link` component enables client-side navigation between two pages in the same Next.js app.
    - Client-side navigation means that the page transition happens using JavaScript, which is faster than the default navigation done by the browser.
  - Next.js does code splitting automatically, so each page only loads what’s necessary for that page. That means when the homepage is rendered, the code for other pages is not served initially.
    - whenever Link components appear in the browser’s viewport, Next.js automatically prefetches the code for the linked page in the background.
- Assets, Metadata, and CSS
  - Next.js has built-in support for CSS and Sass.
  - Next.js can serve static assets, like images, under the top-level `public` directory. Files inside `public` can be referenced from the root of the application similar to `pages`.
    - The `public` directory is also useful for `robots.txt`, Google Site Verification, and any other static assets.
    - 



### [React Context for Beginners](https://www.freecodecamp.org/news/react-context-for-beginners/)

## Videos

### [Why I’m using Next.js in 2020](https://www.youtube.com/watch?v=rtgbaKBhdkk)

### [Learn useContext In 13 Minutes](https://www.youtube.com/watch?v=5LrDIWkK_Bc)

## Bookmark & Review

### [Next.js Examples](https://github.com/vercel/next.js/tree/canary/examples)

## Reading Questions

- What is React Context, and how does it help in managing state and data sharing in a React application?

- Explain the useContext Hook and how it can be used to access data from a React Context within a functional component.

- Describe the purpose of Next.js, and provide an example from the Vercel Next.js Examples reading on how it can be used to build a scalable web application.
