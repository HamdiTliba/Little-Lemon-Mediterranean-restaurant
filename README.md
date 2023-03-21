# Table of Contents

- [Table of Contents](#table-of-contents)
- [The Booking App](#the-booking-app)
- [Setup and Evaluation](#setup-and-evaluation)
- [Front-end Architecture](#front-end-architecture)
  - [Folder Structure](#folder-structure)
  - [Component Architecture](#component-architecture)
  - [Naming Conventions](#naming-conventions)
  - [Use of Dependencies](#use-of-dependencies)
  - [Data Fetching](#data-fetching)
  - [Unit Testing](#unit-testing)
- [Future Considerations](#future-considerations)
- [Honour Code](#honour-code)

---

# The Booking App

This Booking App was created as the final capstone project of the **Meta Front-End Developer Certification**.

**Preview**: Little Lemon is a family-owned Mediterranean restaurant that blends traditional recipes with a modern twist. Our goal is to provide our customers with a unique dining experience that will take them on a culinary journey through the Mediterranean.

**Instructions Received**: To create a modern responsive Front-end for the Little Lemon app with a Bookings feature which they lack at present.

---

# Setup and Evaluation

```s
# Run in the Terminal
git clone https://github.com/HamdiTliba/Little-Lemon-Mediterranean-restaurant.git folder

# Install Dependencies
npm install

# Launch app in Browser
npm start

# Run Tests
npm test

# Run Tests with Coverage
npm test:cv
```

---

# Front-end Architecture

There were several considerations for the frontend architecture.

1. **Folder Structure** - How would the files be organized in the `src` folder.
2. **Component Architecture** - How best to write reusable components.
3. **Naming Conventions** - How and why CSS classes, CSS Variables are named so.
4. **Use of Dependencies** - Choice on what dependencies to use.
5. **Data Fetching** - How we will manage the data used by the app.
6. **Unit Testing** - How to have good coverage in our unit tests.

---

## Folder Structure

Separate folders for:

- **components**: For individual components. Complex components have nested `components` folder. The component folder has 4 files usually (some components are auto-tested without having to create a separate test file. Thus a single folder inside the `components` folder is all inclusive as a single Unit having the Renderer, the stylesheet and the unit test.

  - `Component.jsx` (The Component)
  - `Component.css` (The stylesheet)
  - `index.js` (For exporting the component)
  - `Component.test.jsx` (Test file for the component)

- **pages**: Single Pages in the application that have a collection of these components laid out in different ways. The individual pages in the `pages` folder, may further optionally have a `components` (which represent sections, e.g. `Testimonials`) and optionally, a `pages` (for nested pages) folder in them.

- **context**: Contains Context Providers and basic hooks to access the Context data.
- **hooks**: Hooks unrelated to context. E.g. `useWindowResize` to track resizing the window.
- **actions**: Reducer function and initial states (and any hooks related to them)
- **utilities**: Utility functions. E.g. `validateNumber`.
- **settings**: Contains global settings. Has a `cms` folder that mocks a content management system from which we can source content for our pages. Can be internationalized later.


