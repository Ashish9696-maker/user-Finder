# Dynamic User Search UI

This project is a simple, modern user search interface built with HTML, CSS, and JavaScript. It demonstrates how to dynamically filter and display user profiles as you type into a search bar. The design features a sleek, dark aesthetic with blurred background effects for each user card.

## ✨ Features

  * **Live Search Filter:** Users are filtered in real-time as you type, providing an instant and responsive search experience.
  * **Dynamic UI Generation:** User cards are created and rendered dynamically from a JavaScript array, making the project easily scalable.
  * **Aesthetic Design:** The UI includes a blurred background effect that complements the main profile image, giving it a stylish and polished look.

-----

## 🛠️ Technologies Used

  * **HTML:** Structures the main page, including the search input and the container for the user cards.
  * **CSS:** Styles the UI, defining the layout, colors, and the unique card effects. Tailwind CSS is used to simplify the styling of the main layout.
  * **JavaScript:** Manages the core logic of the application, handling user data, generating the UI, and filtering the users based on the search input.

-----

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd <project-folder>
    ```
3.  **Open `index.html` in your web browser:**
    Simply double-click the `index.html` file, or open it from your browser's file menu. The project runs entirely on the client side, so no server is needed.

-----

## ✍️ Code Overview

### `index.html`

This file sets up the basic structure of the page. It includes a single input field for searching and a `div` with the class `cards` where the user profiles will be displayed. It also links to the Tailwind CSS CDN and the local `style.css` and `script.js` files.

### `style.css`

This file handles the visual design. Key styling includes:

  * A dark background for the body.
  * The `.card` class which sets up the container for each user.
  * The `.blurred-layer` class which creates the unique blurred background effect using a combination of `filter: blur()` and a `mask-image` to create a gradient-like fade.

### `script.js`

This is where the main functionality resides.

1.  A `users` array stores the data for each user, including their name, picture, and bio.
2.  The `showUsers` function iterates through an array of users, creating and appending the necessary HTML elements (`div`, `img`, `h3`, `p`) to the DOM for each user.
3.  An event listener is attached to the search input (`.inp`). Every time the input value changes, it filters the `users` array using the `startsWith()` method.
4.  The content of the `.cards` container is cleared, and the `showUsers` function is called again with the filtered list of users, effectively updating the UI in real-time.
