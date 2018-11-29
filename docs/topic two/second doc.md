---
Title: Second doc title
Description: Second doc description
---

# This is my second doc

It has some content in it.

- [Link to topic 1](../topic-one)
- [Link to item in topic 1](../topic-one/first-doc.md)
- [Link to topic 3](../topic-three)
- [Link to item in topic 3](../topic-three/third-doc.md)

Also some `javascript` code!

```javascript
module.exports = ({ node, getNode }) => {
  // Find the file node.
  let fileNode = node
  let whileCount = 0

  while (
    fileNode.internal.type !== `GitFile` &&
    fileNode.parent &&
    getNode(fileNode.parent) !== undefined &&
    whileCount < 101
  ) {
    fileNode = getNode(fileNode.parent)
    whileCount += 1

    if (whileCount > 100) {
      console.log(
        `It looks like you have a node that's set its parent as itself`,
        fileNode
      )
    }
  }

  return fileNode
}
```

And some code using `js` instead:

```js
  console.log('Hi mum!');
```

And some Java:

```java
class HelloWorldApp {
    public static void main(String[] args) {
        System.out.println("Hello World!"); // Prints the string to the console.
    }
}
```

And `HTML`:

```html
<html>
  <head>
  <title>Title here</title>
  </head>
  <body>
    <p>Hello world!</p>
    <a href="/">Return home</a>
  </body>
</html>
```

```css
p a {
  background: url('../pic.png') center center no-repeat;
  font: bold 15px arial, sans-serif;
}

.intrinsic-16x9 {
  position: relative;
  padding-bottom: 56.25%;
}

```

Finally, some `YAML`:

```yaml
- topic-one:
    title: One
    children:
    - subtopic-one:
        title: 'First subtopic'
        children:
        - first-subtopic-doc.md:
            title: 'Hidden Secrets'
    - first-doc.md: 'First document'
- 'topic two': 'Two'
```
