# MegaBlog: A Modern Full-Stack Blogging Platform

MegaBlog is a feature-rich, full-stack blogging application built with a modern tech stack. It provides a seamless and intuitive experience for both readers and authors, featuring secure authentication, a powerful rich text editor, and dynamic content filtering.

**Live Demo:** https://megablog-1.netlify.app/

<br>

**Homepage & All Posts Section**
<img width="1898" height="918" alt="image" src="https://github.com/user-attachments/assets/1708fb2c-4411-490f-a30c-ea79b8a76227" />
<br>

**Rich Text Editor for Creating & Editing Posts**
<img width="1901" height="913" alt="image" src="https://github.com/user-attachments/assets/a5f5c0cd-3415-4892-95ef-2b18a1e2bec0" />



---

## Features

-   **Full CRUD Functionality:** Create, Read, Update, and Delete posts.
-   **Secure User Authentication:** Users can sign up, log in, and log out securely. Only authenticated users can create, edit, or delete their own posts.
-   **Rich Text Editor:** Powered by **TinyMCE**, allowing authors to easily format their posts with headings, lists, bold, italics, and more.
-   **Dynamic Topic Filtering:** Posts can be assigned topics, and users can filter the articles on the homepage by selecting a topic.
-   **Featured Article Section:** The homepage highlights the most recent post in a prominent featured section.
-   **Fully Responsive Design:** A beautiful and functional UI that works seamlessly on all devices, from mobile phones to desktops, built with **Tailwind CSS**.
-   **Centralized State Management:** Uses **Redux Toolkit** to efficiently manage global state for user authentication and post data.

---

## Tech Stack

-   **Frontend:**
    -   React.js (with Vite)
    -   React Router DOM
    -   Redux Toolkit
    -   Tailwind CSS
-   **Backend (BaaS):**
    -   **Appwrite:** Used for authentication, database (posts), and storage (featured images).
-   **Text Editor:**
    -   TinyMCE Rich Text Editor

---

## Setup and Installation

Follow these steps to get the project running on your local machine.

### Prerequisites

-   Node.js (v18 or later)
-   npm or yarn
-   An active Appwrite instance

### Installation

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/megablog.git](https://github.com/your-username/megablog.git)
    cd megablog
    ```

2.  **Install dependencies:**
    ```sh
    npm install
    ```

3.  **Set up Environment Variables:**
    Create a `.env` file in the root of the project and add the following variables with your Appwrite project credentials:

    ```env
    VITE_APPWRITE_URL="YOUR_APPWRITE_ENDPOINT"
    VITE_APPWRITE_PROJECT_ID="YOUR_PROJECT_ID"
    VITE_APPWRITE_DATABASE_ID="YOUR_DATABASE_ID"
    VITE_APPWRITE_COLLECTION_ID="YOUR_POSTS_COLLECTION_ID"
    VITE_APPWRITE_BUCKET_ID="YOUR_IMAGES_BUCKET_ID"
    ```

4.  **Run the development server:**
    ```sh
    npm run dev
    ```

The application should now be running on `http://localhost:5173`.

---

## Appwrite Collection Setup

For the application to work correctly, your Appwrite "Posts" collection must have the following attributes:

-   `title` (String, required)
-   `content` (String, required)
-   `featuredImage` (String, required)
-   `status` (String, required)
-   `userId` (String, required)
-   `authorName` (String, required)
-   `createdAt` (String, required)
-   `topic` (String, required)

---

## Acknowledgements

This project was built as part of a learning journey, inspired by modern web development best practices and design patterns.
