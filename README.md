# 🏷️ svelte-tags-input

Svelte tags input is a component to use with [Svelte](https://svelte.dev/) and easily enter tags and customize some functions.

## Example

[Live Demo](#)

## Install

```bash
npm install svelte-tags-input --save
```

```javascript
import Tags from "svelte-tags-input";

// If on:tags is defined
let tag = "";

function handleTags(event) {
    tag = event.detail.tags;
}		

<Tags />
```

## Props

#### on:tags
To get the values.

e.g. `on:tags={handleTags}` or `on:tags={getTags}`

##### **dont change `on:tags`**
---

#### addKeys
You can set which keys add new values.

e.g. `addKeys={[9]}` or `addKeys={[9,188]}`

##### **default: 13 (enter)**
---

#### removeKeys
You can set which keys remove new values.

e.g. `removeKeys={[9]}` or `removeKeys={[9,188]}`

##### **default: 8 (backspace)**
---

#### maxTags
You can set maximum number of tags.

e.g. `maxTags={[3]}`

##### **default: false (infinite)**
---

#### onlyUnique
You can set the entered tags to be unique.

e.g. `onlyUnique={true}`

##### **default: false**
---

#### placeholder
You can set a placeholder.

e.g. `placeholder={"Svelte Tags Input"}`

##### **default: empty**
---

```javascript
<Tags
    on:tags={handleTagProperties}
    addKeys={[9]} // TAB Key
    maxTags={3}
    onlyUnique={true}
    removeKeys={[27]} // ESC Key
    placeholder={"Svelte Tags Input"}
/>
```

## CSS

[Download CSS file](#)