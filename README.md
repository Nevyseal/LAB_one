 //This is a  code  that Create an HTML file and add the necessary elements, such as input fields or checkboxes, to allow the user to set their preferences. Additionally, include a button to save the preferences and another button to retrieve the saved preferences.

!DOCTYPE html>
<html>
<head>
    <title>User Preferences</title>
    <script src="script.js"></script>
</head>
<body>
    <h1>User Preferences</h1>
    
    <label for="darkMode">Dark Mode:</label>
    <input type="checkbox" id="darkMode">
    
    <button onclick="savePreferences()">Save Preferences</button>
    <button onclick="retrievePreferences()">Retrieve Preferences</button>
</body>
</html>


/ This is a code that creates a JavaScript file (script.js) and implement the necessary functions to save and retrieve the user preferences using local storage.
/ Save preferences to local storage

function savePreferences() {
    // Get the value of the darkMode checkbox
    const darkMode = document.getElementById("darkMode").checked;
    
    // Store the preferences in local storage
    localStorage.setItem("darkMode", darkMode);
    
    alert("Preferences saved!");
}

// Retrieve preferences from local storage
function retrievePreferences() {
    // Get the saved preferences from local storage
    const darkMode = localStorage.getItem("darkMode");
    
    // Set the checkbox value based on the saved preferences
    document.getElementById("darkMode").checked = JSON.parse(darkMode);
    
    alert("Preferences retrieved!");
}

