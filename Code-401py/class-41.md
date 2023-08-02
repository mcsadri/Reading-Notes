# React 4

## Reading

### [Next.js - Dynamic Routes](https://nextjs.org/learn/basics/dynamic-routes)

- How to statically generate pages with dynamic routes using `getStaticPaths`.
  - Next.js allows you to statically generate pages with paths that depend on external data. This enables dynamic URLs in Next.js.
  - Pages that begin with [ and end with ] are dynamic routes in Next.js.

- How to write `getStaticProps` to fetch the data for each blog post.

- How to render markdown using `remark`.

- How to pretty-print date strings.

- How to link to a page with dynamic routes.

- Some useful information on dynamic routes.

### [Next.js - Deployment](https://nextjs.org/learn/basics/deploying-nextjs-app)

## Video

### [Next.js 10 is here](https://www.youtube.com/watch?v=JWCS5IdECVI)

## Bookmark & Review

### [Next.js - Static File Serving](https://nextjs.org/docs/basic-features/static-file-serving)

## Reading Questions

- Explain the concept of dynamic routes in Next.js and how they differ from static routes.
  - Dynamic routes allow you to create pages with paths that depend on external data or URL parameters.
    - The content of dynamic routes is generated at runtime when a user requests the page.
  - Static routes represent pages that are pre-rendered at build time.
    - Content is generated during the build process and remains the same until the next build.

- Describe the process of deploying a Next.js application. What are the key steps involved, and what are some deployment platforms you can use?
  - Prepare the application for production.
  - Choose a deployment platform.
  - Configure deployment settings.
  - Build the application.
  - Deploy the application.
  - Test and monitor the deployed application.
  - Set up custom domains and SSL for secure access.

- How does Next.js handle static file serving? Discuss the default folder structure for storing static assets and explain how to reference them in a Next.js application.
  - Next.js handles static file serving by serving assets from a folder named `public` at the root of the project, allowing access to files like images and stylesheets.
  - In a Next.js application static files are placed inside the `public` folder at the root of the project. Once stored in the public folder, regular HTML tags are used the React components to include the assets.
