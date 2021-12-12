---
marp: true
---

# How Browser Works + Renders

![bg](https://pbs.twimg.com/media/E3sXKUHVoAEpnUU?format=jpg&name=small)

*2021.Dec.*
Product Team
FE engineer
박세문

---

# 시작하며

## How Browser works

- Tali Garsiel이
- [HTML5ROCKS](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)에 작성한 글 (10년전)

---

## Why

- Performance
- Expandable concept


---

# Good To know

아래에 대해서 알고 있으면 좋습니다

- Tree

![bg right](./assets/tree.png)

---

- Composition

![bg right](./assets/compositing.png)



---

# What is Browser

![bg right 90%](./assets/interface.png)

___


# Browser's High level structure

![bg left 90%](./assets/layers.png)
- 사용자 인터페이스
- 브라우저 엔진
- 렌더링 엔진
- 통신
- JSInterpreter
- Data Persistence

---

# Rendering?

![bg right 90%](./assets/rendering.jpeg)


---

# Rendering in Browser

![bg left vertical 60%](./assets/blink.jpg)
![bg left vertical 30%](./assets/gecko.png)
![bg left vertical 30%](./assets/webkit.jpeg)

---

# Main flow

![bg right 100%](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/flow.png)

1. Parse HTML -> DOM Tree
2. Parse CSS & styles -> attact to Dom Tree
3. Build Render Tree
4. Layout Render Tree
5. Draw Render Tree

---

![w:1200 ](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/webkitflow.png)

---

# HTML Parser

- [Naver D2 blog](https://d2.naver.com/helloworld/59361)
- [HTML5Rocks](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
- [Chromium inside Browser Pt3](https://developers.google.com/web/updates/2018/09/inside-browser-part3?hl=ko)

- `.html` -> `DOM tree`
---

![w:1200](https://developers.google.com/web/updates/images/inside-browser/part3/dom.png?hl=ko)


---

# CSS Parser 

![bg right 90%](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/image023.png)

- [Creating Render tree](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction?hl=ko)

---

# Render Tree

```
class RenderObject{
  virtual void layout();
  virtual void paint(PaintInfo);
  virtual void rect repaintRect();
  Node* node;  //the DOM node
  RenderStyle* style;  // the computed style
  RenderLayer* containgLayer; //the containing z-index layer
}
``` 

---
![w:1200](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/images/render-tree-construction.png?hl=ko)


---

# Layout

---

# Paint 

---

# Performance

- [Reference](https://web.dev/why-speed-matters/) 
  - 한글페이지 있음. 그러나 엔지니어는 영어로 보는걸 추천, 번역이 왈도체...

---

# Loading performance

### TBC

---

# Rendering performance

### TBC

---