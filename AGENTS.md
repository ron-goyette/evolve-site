# Astro Project Context & Agent Rules

You are assisting with an Astro web project. Follow these core architectural rules and best practices to ensure high-performance, static-first output.

## 1. Component Strategy & Hydration
* **Static First:** Default to building UI using standard Astro components (`.astro` files) for all layouts, SEO metadata, and non-interactive elements. 
* **Framework Components:** Only use UI framework components (React, Vue, Svelte, etc.) when client-side state or interactivity is strictly required.
* **Hydration Directives:** Whenever you use a framework component inside an `.astro` file, you MUST include a client directive (e.g., `client:load`, `client:visible`, `client:idle`, or `client:only`) or the component will not be interactive.

## 2. Routing & Content
* **Routing:** Utilize Astro's file-based routing system within the `src/pages/` directory for static pages, dynamic routes, and middleware. 
* **Content Management:** Use Astro Content Collections (`src/content/`) for managing markdown/MDX data, and ensure collections are strictly typed in `src/content/config.ts`[cite: 1].
* **Internationalization:** When implementing multiple languages, utilize Astro's built-in i18n routing and configuration[cite: 1].

## 3. Styling
* **Tailwind CSS:** Use Tailwind utility classes for styling components and layouts[cite: 1]. Avoid creating separate CSS files unless absolutely necessary for complex animations or global base overrides.

## 4. Development & Server Management
When starting or managing the dev server, use the following background mode commands:
* Start server: `astro dev --background`[cite: 1]
* Stop server: `astro dev stop`[cite: 1]
* Check status: `astro dev status`[cite: 1]
* View logs: `astro dev logs`[cite: 1]

## 5. Reference Documentation
If you encounter edge cases or need to implement complex features, consult the full documentation at https://docs.astro.build[cite: 1] or read the specific guides for:
- Routing: https://docs.astro.build/en/guides/routing/[cite: 1]
- Astro Components: https://docs.astro.build/en/basics/astro-components/[cite: 1]
- Framework Components: https://docs.astro.build/en/guides/framework-components/[cite: 1]
- Content Collections: https://docs.astro.build/en/guides/content-collections/[cite: 1]
- Styling/Tailwind: https://docs.astro.build/en/guides/styling/[cite: 1]
- Internationalization (i18n): https://docs.astro.build/en/guides/internationalization/[cite: 1]
