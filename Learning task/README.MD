To create a Next.js homepage using TypeScript and JSX, following the Neumorphism UI design concept, we will use basic HTML elements styled with soft shadows and light backgrounds to achieve the Neumorphism effect.

Steps:

1. Set up a Next.js project with TypeScript.


2. Build the homepage component.


3. Apply Neumorphism styles using CSS.



1. Setup Next.js with TypeScript

If you haven’t already, create a new Next.js app with TypeScript:

npx create-next-app@latest my-neumorphism-app --typescript

Navigate to the project directory:

cd my-neumorphism-app

2. Homepage Component with Neumorphism Design

pages/index.tsx

Here’s a basic homepage built using Neumorphism:

import React from 'react';
import Head from 'next/head';
import styles from '@/styles/Home.module.css';  // Import CSS module

const HomePage: React.FC = () => {
  return (
    <div className={styles.container}>
      <Head>
        <title>Neumorphism Homepage</title>
        <meta name="description" content="A simple Next.js homepage with Neumorphism UI" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
      </Head>
      
      <main className={styles.main}>
        <h1 className={styles.title}>Welcome to Neumorphism UI</h1>
        
        <div className={styles.card}>
          <p>Neumorphism gives the soft, 3D look.</p>
          <button className={styles.button}>Get Started</button>
        </div>
      </main>
    </div>
  );
};

export default HomePage;

3. Neumorphism CSS

To achieve the Neumorphism UI effect, we use soft shadows and light backgrounds. You can apply this with CSS. Let's create a CSS file that implements the Neumorphism styles.

styles/Home.module.css

/* General Container */
.container {
  display: flex;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  background-color: #e0e0e0;
  padding: 0 2rem;
}

/* Main Section */
.main {
  text-align: center;
}

.title {
  font-size: 2.5rem;
  color: #333;
  margin-bottom: 2rem;
}

/* Neumorphic Card */
.card {
  background: #e0e0e0;
  border-radius: 20px;
  box-shadow: 10px 10px 30px #bebebe, -10px -10px 30px #ffffff;
  padding: 2rem;
  max-width: 400px;
  margin: 0 auto;
}

.card p {
  font-size: 1.25rem;
  color: #555;
}

/* Neumorphic Button */
.button {
  background: #e0e0e0;
  border-radius: 50px;
  border: none;
  padding: 1rem 2rem;
  font-size: 1rem;
  color: #333;
  box-shadow: 5px 5px 15px #bebebe, -5px -5px 15px #ffffff;
  cursor: pointer;
  transition: all 0.3s ease;
}

.button:hover {
  box-shadow: inset 5px 5px 15px #bebebe, inset -5px -5px 15px #ffffff;
}

.button:active {
  box-shadow: inset 2px 2px 5px #bebebe, inset -2px -2px 5px #ffffff;
}

4. Explanation of Neumorphism Design Elements

Container: The background color is light grey (#e0e0e0) to create a neutral base.

Shadows: To create the 3D, soft effect:

Box-shadow: A combination of dark and light shadows (#bebebe and #ffffff) creates the raised effect.

Hover/Active effects: Changes in shadow on hover and active states give it an interactive feel.


Button: A rounded button that also uses Neumorphism with soft shadows and reacts when clicked or hovered.


5. Running the Project

Run the following commands to start the development server:

npm run dev

Visit http://localhost:3000 to see your Neumorphism homepage in action.


---

This basic Neumorphism UI design can be extended with more components, like cards, inputs, and more complex layouts, while adhering to the soft, 3D-like visual style.
