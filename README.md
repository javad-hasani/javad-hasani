<div align="center">

# Hi, I'm Javad Hasani 👋

### Front-End Developer · Next.js Enthusiast · UI Builder

[![GitHub followers](https://img.shields.io/github/followers/javad-hasani?style=for-the-badge&logo=github&label=Followers&color=0891b2)](https://github.com/javad-hasani?tab=followers)
![Profile views](https://komarev.com/ghpvc/?username=javad-hasani&style=for-the-badge&color=0891b2)

</div>

## About me

I'm a 31-year-old front-end developer from Shiraz, Iran. I enjoy turning ideas into clean, responsive interfaces and experimenting with colors, interactions, and modern web technologies.

- 🔭 Building modern web experiences with React and Next.js
- 🌱 Continuously improving my Next.js and front-end architecture skills
- 🤝 Open to collaborating on interesting web projects
- 💬 Feedback and constructive criticism are always welcome
- 📫 Reach me at [javadhasani93@yahoo.com](mailto:javadhasani93@yahoo.com)

## Tech stack

<p align="left">
  <img src="https://skillicons.dev/icons?i=js,html,css,react,nextjs,redux,tailwind,bootstrap,jquery,vite,photoshop&perline=11" alt="JavaScript, HTML, CSS, React, Next.js, Redux, Tailwind CSS, Bootstrap, jQuery, Vite and Photoshop" />
</p>

## 🎮 Mini game: Spot the Bug

Three bugs are hiding below. Try to solve each one before opening the answer.

<details>
<summary><strong>Level 1 · Why does this log 3 three times?</strong></summary>

```js
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 100);
}
```

<details>
<summary>Reveal the answer</summary>

`var` creates one function-scoped binding shared by every callback. When they run, the loop has already finished and `i` is `3`.

Fix it with `let`:

```js
for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 100);
}
```

</details>
</details>

<details>
<summary><strong>Level 2 · Why doesn't the React UI update?</strong></summary>

```jsx
const [user, setUser] = useState({ name: "Javad", score: 0 });

function levelUp() {
  user.score += 1;
  setUser(user);
}
```

<details>
<summary>Reveal the answer</summary>

The existing state object is mutated and then passed back with the same reference. React may skip the render.

```jsx
function levelUp() {
  setUser(current => ({ ...current, score: current.score + 1 }));
}
```

</details>
</details>

<details>
<summary><strong>Level 3 · Find the Next.js hydration trap</strong></summary>

```jsx
export default function Clock() {
  return <p>{new Date().toLocaleTimeString()}</p>;
}
```

<details>
<summary>Reveal the answer</summary>

The server and browser can render different times, so their first HTML output may not match. Render the live value after the component mounts.

```jsx
"use client";

import { useEffect, useState } from "react";

export default function Clock() {
  const [time, setTime] = useState("");

  useEffect(() => {
    setTime(new Date().toLocaleTimeString());
  }, []);

  return <p>{time || "Loading time..."}</p>;
}
```

</details>
</details>

<div align="center">

### My GitHub activity

<img height="165" src="https://github-readme-stats.vercel.app/api?username=javad-hasani&show_icons=true&theme=tokyonight&hide_border=true" alt="Javad's GitHub stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=javad-hasani&layout=compact&theme=tokyonight&hide_border=true" alt="Javad's most used languages" />

### Let's connect

[![GitHub](https://img.shields.io/badge/GitHub-javad--hasani-181717?style=for-the-badge&logo=github)](https://github.com/javad-hasani)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Javad_Hasani-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/javad-hasani)
[![Instagram](https://img.shields.io/badge/Instagram-@_javadhasani-E4405F?style=for-the-badge&logo=instagram)](https://www.instagram.com/_javadhasani)
[![Threads](https://img.shields.io/badge/Threads-@_javadhasani-000000?style=for-the-badge&logo=threads)](https://www.threads.net/@_javadhasani)

</div>
