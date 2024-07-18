# Event Landing Page

## Description

This project is a Vue.js 3 application that creates a responsive event landing page with a registration form. It's designed for a webinar titled "How to Integrate GenAI into CX: Balancing Innovation with Safety & Security". The page includes sections for event details, speaker information, and a comprehensive registration form with validation.

## Contents

The project consists of the following main components:

1. `App.vue`: The main component that structures the entire landing page.
2. `RegistrationForm.vue`: A component that handles the registration form with validation.

Key features include:

- Responsive design for both desktop and mobile views
- Dynamic speaker information display
- A registration form with real-time validation
- Country selection options

## Technologies Used

- Vue.js 3 (with Composition API)
- Tailwind CSS for styling
- Vite as the build tool

## Installation

To set up this project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone [repository-url]
   cd event-landing-page-test
   cd app
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Install Tailwind CSS:

   ```bash
   npm install -D tailwindcss@latest postcss@latest autoprefixer@latest
   npx tailwindcss init -p
   ```

4. Configure Tailwind CSS:
   Create a `tailwind.config.js` file in the root directory with the following content:

   ```javascript
   module.exports = {
     content: [
       "./index.html",
       "./src/**/*.{vue,js,ts,vue,tsx}",
     ],
     theme: {
       extend: {},
     },
     plugins: [],
   }
   ```

5. Add Tailwind directives to your CSS:
   In your main CSS file (e.g., `src/assets/main.css`), add:

   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

6. Run the development server:

   ```bash
   npm run dev
   ```

7. Build for production:

   ```bash
   npm run build
   ```

## Usage

After starting the development server, you can view the landing page at `(whichever port Vite assigns)`. 

The registration form includes validation for all fields and will only submit when all required fields are correctly filled.
