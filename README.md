#  [Password-Generator](https://www.google.com/)

This project is a Random Password Generator that enables users to create secure passwords with customizable features. Users can specify the length of the password and the types of characters to include (lowercase, uppercase, numbers, symbols). It also includes a copy-to-clipboard feature for convenience. <br/>
## Features
- Customizable Password Length: Adjustable between 8 and 20 characters. 
- Character Options: 
    1.  Include lowercase letters (a-z).
    2.	Include uppercase letters (A-Z).
    3.	Include numbers (0-9).
    4.	Include symbols (e.g., @, #, $).
+	Responsive Slider: Dynamically updates the selected password length.
+	Clipboard Copy Functionality: Quickly copy the generated password.
+	Material Icons and Google Fonts: Enhance the UI for a sleek and modern look.
## Technologies Used
*	HTML5
*	CSS3
*	JavaScript (ES6)
*	Google Fonts
*	Material Icons
## How to Use
1.	Open the application in any modern browser.
2.	Use the slider to select the desired password length.
3.	Check the boxes for the character types you want to include: 
    +	Lowercase letters
    +	Uppercase letters
    +	Numbers
    +	Symbols
4.	Click the "Generate Password" button to create a password.
5.	To copy the generated password, click the clipboard icon. The icon will briefly change to indicate success. <br/>
File Structure <br/>
project-directory/ <br/>
├── index.html        # Main HTML file <br/>
├── style.css         # Styling for the UI  <br/>
├── script.js         # JavaScript logic for password generation <br/>
Code Highlights
+	**Dynamic Slider Updates:**
```git
	inputSlider.addEventListener("input", () => {
	    sliderValue.textContent = inputSlider.value;
	});
```
+	**Password Generation Logic:**
```git
	function generatePassword() {
	    const length = inputSlider.value;
	    let characters = "";
	    characters += lowercaseEl.checked ? lowercaseLetters : "";
	    characters += uppercaseEl.checked ? uppercaseLetters : "";
	    characters += numberEl.checked ? numbers : "";
	    characters += symbolsEl.checked ? symbols : "";
	    let password = "";
	    for (let i = 0; i < length; i++) {
	        password += characters.charAt(Math.floor(Math.random() * characters.length));
	    }
	    return password;
	}
```
+	**Clipboard Copy Feedback:**
```git
	copyIcon.addEventListener("click", () => {
	    if (passBox.value !== "" && passBox.value.length >= 10) {
	        navigator.clipboard.writeText(passBox.value);
	        copyIcon.innerText = "check";	
	        setTimeout(() => {
	            copyIcon.innerHTML = "content_copy";
	        }, 1000);
	    }
	});
```
## Possible Enhancements
*   Add validation to ensure at least one character type is selected.
*	Use crypto.getRandomValues() for better randomness.
*	Improve accessibility with ARIA labels for interactive elements.
*	Style the password field for better visibility.
## License
This project is open-source and available under the MIT License. Feel free to customize and extend this project as needed!
## Contact
For any inquiries or to connect: <br/>
Email: amanajaz990@gmail.com <br/>
GitHub: [Iamanajaz](https://www.gitnub.com/Iamanajaz)


