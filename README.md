# OOP Concepts with Next.js: Simple Publication Collection Manager

This is a mini-project demonstrating Object-Oriented Programming (OOP) concepts using JavaScript within a Next.js application. It implements a simple collection manager for publications like books and magazines.

The primary goal of this project is to illustrate how core OOP principles – Encapsulation, Abstraction, Inheritance, and Polymorphism – can be applied in a modern JavaScript and React environment.

## OOP Concepts Demonstrated

This project explicitly showcases the following OOP principles:

1.  **Encapsulation:**
    * Data (properties) and methods that operate on that data are bundled together within classes (`PublicationItem`, `Book`, `Magazine`, `Library`).
    * Internal state of objects (e.g., the `items` array in the `Library` class) is managed internally and accessed or modified through public methods, hiding the implementation details.

2.  **Abstraction:**
    * Complex implementation details are hidden behind a simplified interface. For example, users of the `Library` class interact with methods like `addItem()` or `getAllItems()` without needing to know the specifics of how the collection is stored or managed.
    * The `getDetails()` method on `PublicationItem` provides a common way to get a description, abstracting away the specific type of publication.

3.  **Inheritance:**
    * A base class `PublicationItem` is defined with common properties (`id`, `title`) and methods.
    * `Book` and `Magazine` classes **inherit** from `PublicationItem`, reusing common functionality and extending it with their specific attributes (e.g., `author` and `year` for `Book`; `publisher` and `issueNumber` for `Magazine`).
    * The `super()` keyword is used in derived class constructors to call the parent class constructor.

4.  **Polymorphism:**
    * **Method Overriding:** The `getDetails()` method is defined in the `PublicationItem` base class and then overridden in both `Book` and `Magazine` derived classes to provide type-specific details.
    * **Dynamic Behavior:** When iterating through a collection of `PublicationItem` objects, calling `item.getDetails()` executes the appropriate version of the method based on the actual type of the object (`Book` or `Magazine`). This allows treating objects of different classes in a uniform way through a common interface.
    * The `Library.addItem(item)` method also demonstrates polymorphism as it can accept any object that is an instance of `PublicationItem` or its subclasses.

## Project Structure Highlights

* `src/lib/models.js`: Contains all the JavaScript class definitions (`PublicationItem`, `Book`, `Magazine`, `Library`) demonstrating the OOP structure.
* `src/app/page.js`: The main Next.js page component that utilizes these classes to manage and display the publication collection. It handles user input, state management (using React Hooks), and renders the UI.

## Features

* Add new publications (Books or Magazines) to the collection with specific details.
* View a list of all publications in the collection.
* Display type-specific details for each publication polymorphically.
* Remove publications from the collection.
* Dynamic form changes based on the selected publication type.

## Tech Stack

* **Next.js (v13+ with App Router)**: React framework for server-side rendering and static site generation.
* **React (v18+)**: JavaScript library for building user interfaces.
* **JavaScript (ES6+)**: Core language, utilizing classes for OOP.
* **CSS**: Minimal inline styling for presentation.

## Setup and Installation

Follow these steps to get the project running locally:

1.  **Prerequisites:**
    * Node.js (v18.x or later recommended)
    * npm or yarn

2.  **Clone the repository:**
    ```bash
    git clone <https://github.com/raisenbk/oop-book-collection-app.git>
    cd oop-book-collection-app
    ```

3.  **Install dependencies:**
    Using npm:
    ```bash
    npm install
    ```
    Or using yarn:
    ```bash
    yarn install
    ```

## Running the Application

1.  **Start the development server:**
    Using npm:
    ```bash
    npm run dev
    ```
    Or using yarn:
    ```bash
    yarn dev
    ```

2.  **Open your browser:**
    Navigate to `http://localhost:3000`. You should see the application running.

## Further Exploration (Optional)

This project serves as a basic example. It could be extended to include:

* More complex class hierarchies.
* Persistent storage (e.g., using `localStorage`, a backend API, or a database).
* Editing existing items.
* Advanced search and filtering capabilities.
* More sophisticated UI/UX with a CSS framework or library.
* Unit tests for the OOP classes.

---

Feel free to explore the code and experiment with the OOP concepts demonstrated!
