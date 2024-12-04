# Redirect-Link

This project is a simple redirect page designed to redirect users to a specified URL after a short delay. It includes branding, a manual redirect button, and the ability to specify the target URL dynamically through query parameters.

---

## Features

- **Dynamic URL Redirect**: Automatically redirects users to a target URL specified in the query parameter `l`.
- **Branding Display**: Shows a logo and message before the redirection.
- **Fallback Manual Button**: Provides a clickable button for manual redirection if the automatic redirect fails.
- **Customizable Delay**: Currently set to 1 second but easily adjustable in the code.

---

## How It Works

1. **Enter the Redirect Page**:
   - Open the URL for the GitHub Pages site where this project is hosted:
     ```
     https://yourusername.github.io/Redirect-Link/
     ```

2. **Add a Target URL**:
   - Add the `?l=` query parameter to the URL, followed by the target link.
   - Example:
     ```
     https://yourusername.github.io/Redirect-Link/?l=https://amzn.to/example
     ```

3. **Redirection Process**:
   - The page will display your logo and a message.
   - After 1 second, the page automatically redirects to the target URL.

4. **Manual Redirect Option**:
   - If the redirect does not happen, the user can click the "Proceed to Amazon" button to be manually redirected.

---

## Installation

### Prerequisites
- A GitHub account.
- A repository with GitHub Pages enabled.

### Steps
1. Clone or create a new repository.
2. Upload the `index.html` file to the root of the repository.
3. Enable GitHub Pages by navigating to **Settings > Pages**, selecting `main` as the branch, and setting the folder to `/ (root)`.

---

## Customization

### 1. **Change the Logo**
- Replace the `SG Dealz 2.png` file in the repository with your own logo.
- Update the `src` attribute in the `<img>` tag in the HTML file.

### 2. **Adjust the Redirect Timer**
- In the script section of `index.html`, change the `1000` in this line to adjust the delay (in milliseconds):
  ```javascript
  setTimeout(() => {
      if (redirectUrl) {
          window.location.href = redirectUrl;
      }
  }, 1000); // Redirect after 1 second (1000ms)
