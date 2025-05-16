# Interact with GitHub Copilot

## Copilot Chat
Ask questions, get explanations, and receive code suggestions in a dedicated chat panel

```plaintext
@workspace /src/utils.js
Can you explain what this file does?
```

## Inline Chat
Interact with Copilot directly in your code editor with context-aware suggestions

```javascript
// With cursor here, press Ctrl+I
function calculateTotalPrice(items) {
  // Implement a function that calculates the total price
  // of all items including tax
}
```

## Comments to Code
Write natural language comments that Copilot converts into executable code

```javascript
// Function to fetch user data from API and format it
// Should handle errors and return a default value if the API fails
// The API endpoint is at https://api.example.com/users
```

Generating the something like this
```javascript
function fetchUserData() {
  return fetch('https://api.example.com/users')
    .then(response => {
      if (!response.ok) {
        throw new Error('Network response was not ok');
      }
      return response.json();
    })
    .then(data => {
      return data.map(user => ({
        id: user.id,
        name: user.name,
        email: user.email
      }));
    })
    .catch(error => {
      console.error('Error fetching user data:', error);
      return [];
    });
}
```