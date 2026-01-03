# Simple Kanban Board (Drag and Drop)

A lightweight, responsive **Kanban Board** built using **HTML, CSS, and Vanilla JavaScript**, demonstrating the native **HTML5 Drag and Drop API**.  
This project is ideal for beginners who want to understand how drag-and-drop interactions work without external libraries or frameworks.

---
## Screenshots
![Quiz Game Start Screen](https://github.com/vishalvermacore/Kanban-Board/blob/ee4cdf1fcf27f3bddd0f18bf12f576597fc553e2/Kanban_Board.png)

---

## 📌 Features

- Three Kanban columns:
  - **To Do**
  - **In Progress**
  - **Done**
- Drag cards between columns
- Smooth animations and visual feedback
- Fully responsive design
- No external dependencies

---

## 🗂️ Project Structure

kanban-board/
│
├── index.html # Markup structure
├── style.css # Styling and layout
├── script.js # Drag and Drop logic
└── README.md # Project documentation


---

## 🚀 Getting Started

### 1. Clone or Download the Project
```bash
git clone https://github.com/your-username/kanban-board.git
```
Or simply download the ZIP file and extract it.

### 2. Open in Browser

Open index.html in any modern web browser (Chrome, Edge, Firefox, Safari).

No server or build tools are required.

---

## 🧠 How It Works
HTML (Structure)

Each card has draggable="true".

Each list (column) acts as a drop zone.

## Key attributes:
```
<div class="card" draggable="true" id="card1">Do Exercise</div>
```

## JavaScript (Logic)

The project uses the HTML5 Drag and Drop API:
| Event       | Purpose                    |
| ----------- | -------------------------- |
| `dragstart` | Stores the dragged card ID |
| `dragover`  | Allows dropping            |
| `dragenter` | Adds visual highlight      |
| `dragleave` | Removes highlight          |
| `drop`      | Moves the card             |
| `dragend`   | Ends drag operation        |

---

## Example:

```js
function dragDrop(e) {
  const id = e.dataTransfer.getData("text/plain");
  const card = document.getElementById(id);
  this.appendChild(card);
}

```
## 📚 Authoritative References

The implementation follows official web standards and documentation:

- **MDN Web Docs – HTML Drag and Drop API**  
  https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API

- **MDN – Using the Drag and Drop API**  
  https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API/Using_the_Drag_and_Drop_API

- **W3C HTML Living Standard (Drag and Drop)**  
  https://html.spec.whatwg.org/multipage/dnd.html

These sources are maintained by **Mozilla** and the **WHATWG** and are considered authoritative references for modern web standards.

---

## 🔧 Possible Enhancements

- Add `localStorage` persistence to retain card state after page refresh
- Create new cards dynamically via user input
- Enable column reordering through drag-and-drop
- Add touch support for mobile drag-and-drop interactions
- Introduce accessibility improvements using ARIA roles and keyboard navigation

---

## 📄 License

This project is open-source and available for educational and personal use.
