// Function to handle the search and redirect
function performSearch() {
    // Get the value from the input field
    const query = document.getElementById('search-input').value.trim();

    // Check if the input field is not empty
    if (query) {
        if (query.includes('.') && !query.startsWith('http')) {
            // If it's a URL without 'http', add 'https://' and redirect
            window.location.href = `https://${query}`;
        } else if (query.includes('.') && query.startsWith('http')) {
            // If the user already typed a full URL with 'http/https', redirect directly
            window.location.href = query;
        } else {
            // Otherwise, treat it as a search query and redirect to Google search
            window.location.href = `https://www.google.com/search?q=${query}`;
        }
    }
}

// Event listeners for button click and "Enter" keypress
document.getElementById('search-btn').addEventListener('click', performSearch);

document.getElementById('search-input').addEventListener('keypress', function (e) {
    // If the Enter key is pressed, perform the search
    if (e.key === 'Enter') {
        performSearch();
    }
});
