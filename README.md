# Public API Quick Tester (Ultra-Light)

A single webpage to quickly hit a public GET API endpoint (no auth) and see the JSON response, without firing up Postman or writing a script.

**Live Demo:** [(https://api-quick-test.pages.dev/)] <!-- Add this after deployment -->

## The Problem

You want to quickly inspect the JSON response from a public GET API endpoint. You don't want the overhead of opening a tool like Postman or writing a quick `curl` or Python script, especially for a one-off check.

## The Solution 

A dead-simple, entirely client-side webpage:
*   One input field for the API URL.
*   A "Go" button.
*   Makes a GET request using client-side JavaScript (`fetch`).
*   Pretty-prints the JSON response (or error message) directly on the page.

## Features

*   **Ultra-Lightweight:** Single HTML file with embedded CSS and JavaScript.
*   **Zero Dependencies:** No external libraries or frameworks.
*   **Client-Side Only:** No backend, no data storage. Your requests go directly from your browser to the API.
*   **Pretty-Printed JSON:** Easy-to-read formatted JSON output.
*   **Error Handling:** Displays HTTP status errors and network errors.
*   **CORS Aware:** Includes a note about Cross-Origin Resource Sharing (CORS) limitations.
*   **Responsive:** Basic responsiveness for different screen sizes.

## How to Use

**Option 1: Use the Live Version**
Visit [(https://api-quick-test.pages.dev/)] <!-- Add this after deployment -->

**Option 2: Run Locally**
1.  Clone this repository or download `index.html`.
2.  Open `index.html` in your web browser.

**Option 3: Deploy Your Own**
This project is a single `index.html` file, making it incredibly easy to deploy on static site hosting platforms like:
*   [Cloudflare Pages](https://pages.cloudflare.com/)
*   [GitHub Pages](https://pages.github.com/)
*   [Netlify](https://www.netlify.com/)
*   [Vercel](https://vercel.com/)

## Important: CORS (Cross-Origin Resource Sharing)

For this tool to work, the target API endpoint **must** have appropriate CORS headers configured to allow requests from the domain where this tool is hosted (or `*` for all origins). If the API doesn't allow cross-origin requests from your browser, the request will be blocked by the browser's security policy, and you'll likely see a network error in the console.

## Technology

*   HTML
*   CSS (inline)
*   Vanilla JavaScript (ES6+ `fetch` API)

## Contributing

Found a bug or have a suggestion? Feel free to open an issue or submit a pull request! Keep it ultra-light!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
