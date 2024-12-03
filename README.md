<section id="logo" align="center">
  <a href="https://animata.design/">
   <h2>Animata</h2>
  </a>
  
  <p>Handcrafted interaction animations and visual effects sourced from across the internet 🛜, ready for you to copy and paste into your project seamlessly.</p>
  <section id="padges" margin="50">
    <h3>Built with</h3>
    <a href="https://nextjs.org/?ref=animata.design">
      <img alt="Next.js" src="https://img.shields.io/badge/Next.js-000?logo=nextdotjs&logoColor=fff&style=for-the-badge"/>
    </a>
    <a href="https://reactjs.org/?ref=animata.design">
      <img alt="React.js" src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
    </a>
    <a href="https://tailwindcss.com/?ref=animata.design">
      <img alt="Tailwind" src="https://img.shields.io/badge/Tailwind_CSS-0b1120?style=for-the-badge&logo=tailwind-css&logoColor=38bdf8"/>
    </a>
    <a href="https://www.framer.com/motion/?ref=animata.design">
      <img alt="Framer Motion" src="https://img.shields.io/badge/Framer-1a1a1a?style=for-the-badge&logo=framer&logoColor=white"/>
    </a>
    <a href="https://www.typescriptlang.org/?ref=animata.design">
      <img alt="Typescript" src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white"/>
    </a>
    <a href="https://vercel.com/?ref=animata.design">
      <img alt="Vercel" src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white"/>
    </a>
  </section>
</section>
<br>

## Introduction

### What is Animata?
Welcome to Animata, a free and open-source collection of hand-crafted animations, effects, and interactions that you can seamlessly integrate into your project with a simple copy and paste. The animations are built using TailwindCSS and React.js, so they can be easily customized to fit your project's design.

### What is not Animata?
Animata is not a full-fledged UI library like Material-UI or Chakra-UI. It is a collection of animations and effects that you can use to enhance your project's design. You can also use Animata alongside other UI libraries or design systems (you will need to set up TailwindCSS for this).

## Getting Started
You don't need to install it as a dependency instead you can simply copy and paste the code, as shadcn/ui, into your project. However, you still need to install the other dependency that the code needs.

### Requirements
- [TailwindCSS](https://tailwindcss.com/docs/installation): For styling.
- [Framer Motion](https://www.framer.com/motion/) (Optional): For complex animations.
- [Lucide Icons](https://lucide.dev/) or [Radix Icons](https://www.radix-ui.com/icons) (Optional): Use for icons, or replace with any other icon library or SVGs.

### Setup Instructions
#### Folder Structure (Recommended)

```bash
/
  /components
  /ui
```

where `/` is the root of your project, `/components` is where you keep your components and the project has been set up using paths in the `tsconfig.json` file.

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["./*"]
    }
  }
}
```
#### Install Dependencies
Install the required dependencies, if you haven't already:

```sh
npm install tailwind-merge clsx lucide-react tailwindcss-animate
```

Add `tailwindcss-animate` to plugins in `tailwind.config.js` file:

```js
module.exports = {
  plugins: [require("tailwindcss-animate")],
};
```

### Create Utility Functions
Create utils.ts file in the libs folder and paste the following code:

```ts
import { type ClassValue, clsx } from "clsx";
import { twMerge } from "tailwind-merge";
 
export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

#### NOTE
1. If you see something that has been imported but not mentioned in the documentation, then it is a dependency you need to install. If it starts with @/ then it is Animata's component else it is an external dependency. In such a case, you can submit a PR to update the documentation.
2. If something is not working, the docs probably miss the tailwind.config.js updates. You can look for the entries that have been added to the tailwind.config.js in Animata's source code. You can create an issue or submit a PR to update the documentation.


