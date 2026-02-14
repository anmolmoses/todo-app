# Ahintodew Design System

## Class Naming: BEM
- Block: `.todo`, `.header`, `.category`, `.filters`
- Element: `.todo__checkbox`, `.todo__label`, `.todo__text`
- Modifier: `.todo--completed`, `.header--sticky`

## HTML Patterns

### Todo Item
```html
<li class="todo">
  <input type="checkbox" id="todo-{id}" class="todo__checkbox">
  <label for="todo-{id}" class="todo__label">
    <span class="todo__checkmark"></span>
    <span class="todo__text">Task text here</span>
    <span class="todo__tag todo__tag--{priority}">Tag</span>
  </label>
</li>
```

### Category Section
```html
<details class="category" open>
  <summary class="category__header">
    <span class="category__icon">{emoji}</span>
    <span class="category__title">Category Name</span>
    <span class="category__count"></span>
    <span class="category__chevron"></span>
  </summary>
  <ul class="category__list">
    <!-- todo items here -->
  </ul>
</details>
```

### Priority Tags
- `.todo__tag--high` (coral/red)
- `.todo__tag--medium` (amber)
- `.todo__tag--low` (teal)

## CSS Counter Names
- `total-tasks` — incremented by each `.todo`
- `completed-tasks` — incremented by `.todo__checkbox:checked`

## Categories (3 total)
1. 🌅 Morning Routine (3 todos)
2. 💼 Work (4 todos)
3. 🌙 Evening (3 todos)

## Z-Index Scale
- --z-bg: 0
- --z-card: 10
- --z-header: 100
- --z-overlay: 200
