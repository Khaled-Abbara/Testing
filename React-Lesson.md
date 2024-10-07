# Summary of Session One

## What is React?
React is a frontend library developed by facebook that uses a virtual DOM to keep track of what the user does  instead of updating the DOM.

## React's design philosophy (React Mentality) 
We divide the website into reusable components, where Each compenent is writen as a function that displays jsx.
the code is written like a root structure of plant or a christmas tree, where one component houses other componenets inside it. This apporach means that the failure of components lower below does not affect the entire website. and that when changes are made due to users actions; the whole site does not have to reload again (more info will be provided below).

## Why React?
1. It's main selling point is by adding logic to HTML in the form of JSX.
2. It introduces a virtual DOM which makes your code base less of a Fettuccine Alfredo in the long run.
3. It's faster and easier to use than 'Vanilla JS'.
4. Alot of companies use it, so there is a good job opportunity (Other frontend librarys are very similar).
5. I like it, and it was What I felt was missing with my Webshop.

## What is jsx
Javascript Extensible Markup Language or Javascript XML is an extenstion to JS, here is an example.

```Javascript
const Monkey = <h1>Hello, Copy Paste Developer!</h1>;
```

This is not HTML inside JS, Infact it is just Javascript playing dress up. JSX is a subset of Javascript.

## What is Typescript
Typescript is a Programing language that is Strongly typed, which means you have to declare the kind of data type inside a variable or perameter. Typescript is a SuperSet of Javascript Which means that TypeScript is basicaly Javascript but with added features.

Here is some example code:
```Typescript
// Data Type | string
const name: string = "khaled";

// Data Type | Number (integer and Floats are number here)
let age: number = 18;

// Data Type | Boolean
var Cool: boolean = true;

// Data Type | Any (This is basically dynamicaly typed)
let car: any = "BMW";

function greeting(name: string, age: number, colourful: boolean) {
console.log("Hi ${name}, you are ${age}, and you are ${Cool}");
}
greeting(name, age, colourful);
```
## What is tsx
It is just like JSX but with The added features of Typescript.

## What is Vite?
Vite is like a server that uses port 5173, it has a Hot Module Replacement (HMR) system, which quickly shows changes on screen from the code that is written, Vite supports frameworks such as React, Vue, Svelte, and many more.

*"Vite is basically the united nations of JavaScript at this point."*

### how to use Vite
1. ```npm create vite@latest```
2. write your Project name
3. write your Package name
4. select a framework using arrow keys
5. select variant
6. ```cd project name```
7. ```npm install```
8. ```npm run dev```

## Hierarchy in React

#### index.html Which containes a react script tag
code:
```HTML 
<script type="module" src="/src/main.tsx"></script>
```

#### main.tsx which containes an 'App' Component
code:
```Javascript
createRoot(document.getElementById('root')!).render(
  <StrictMode>
    <App />
  </StrictMode>,
)
```

#### App.tsx which containes componenets of your liking
code:
```Javascript
function App() {
  return (
    <>
      <Header />
      <SearchBox />
      <Menu />
      <Footer />
    </>
  );
}
```

## tsx is more than HTML
code example:
```tsx
function Animalgen() {
  const animals = ["Cow", "Sheep", "Cat", "Mouse"];

  var index = Math.floor(Math.random() * animals.length);

  return (
    <>
      <p>Here is a random animal {animals[index]}</p>
    </>
  );
}

export default Animalgen;
```
## for Loop in tsx
We can't use a for loop inside the return statment but we can use a map function; there are other ways also

example code:
```tsx
function AnimalList() {
  let animals = ["Monkey", "Rabbit", "Donkey"];

  return (
    <>
      {animals.map((item, index) => (
        <h3>
          {item}'s idex is {index}
        </h3>
      ))}
    </>
  );
}
export default AnimalList;
```
