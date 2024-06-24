# Contact-Page-Layout
A well-designed contact page is essential for any website, providing visitors with an easy way to get in touch with you. Here is a simple description of a basic contact page layout:
![Screenshot (29)](https://github.com/alshahariahossen01/Contact-Page-Layout/assets/144457355/25f7bcef-8739-403c-ad4d-98753a6ab5de)

Header
Title: "Contact Us"
Subtitle: A brief welcoming message or instruction, such as "We'd love to hear from you! Please fill out the form below or use one of the methods to reach us."
Contact Form
Fields:
Name: A text field for the visitor's full name.
Email: A text field for the visitor's email address.
Subject: A text field for the subject of the message.
Message: A larger text area for the visitor to write their message.
Submit Button: A button labeled "Send" or "Submit" to submit the form.
Additional Contact Information
Phone Number: A phone number visitors can call for direct contact.
Email Address: An email address for direct communication.
Physical Address: The physical location of your business, if applicable.
Business Hours: The hours during which you are available.
Map (Optional)
An embedded map showing your physical location.
Social Media Links
Icons and links to your social media profiles (e.g., Facebook, Twitter, LinkedIn).
Footer
Privacy Policy: A link to your privacy policy.
Terms of Service: A link to your terms of service.

Dark mode and light mode option code is here

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="contact-container">
        <div class="mode-toggle-box">
            <button id="mode-toggle">
                <img src="moon.png" alt="Toggle Dark Mode">
                
            </button>
        </div>
        <div class="contact-header">
            <h1>Contact Me</h1>
            <h2>You become what you believe.</h2>
        </div>
        <div class="contact-content">
            <div class="contact-left">
                <div class="box light-box">
                    <div class="social-icon">
                        <img src="share.png" alt="Social Profile">
                    </div>
                    <h3>Social Profile</h3>
                    <div class="social-links">
                        <a href="https://twitter.com/shaharia_munna" target="_blank"><img src="twitter.png" alt="Twitter"></a>
                        <a href="https://facebook.com/alshahariahossen01" target="_blank"><img src="facebook.png" alt="Facebook"></a>
                        <a href="https://instagram.com/alshahariahossen01" target="_blank"><img src="instagram.png" alt="Instagram"></a>
                        <a href="https://linkedin.com/alshahariahossen01" target="_blank"><img src="linkedin.png" alt="LinkedIn"></a>
                    </div>
                </div>
                <div class="contact-info">
                    <div class="box light-box email-box">
                        <h3><img src="email.png" alt="Email"> Email Me:</h3>
                        <p>example@example.com</p>
                    </div>
                    <div class="box light-box call-box">
                        <h3><img src="viber.png" alt="Call"> Call Me:</h3>
                        <p>+123456789</p>
                    </div>
                </div>
            </div>
            <div class="contact-right">
                <form>
                    <div class="input-row">
                        <div class="input-group">
                            <input type="text" id="name" name="name" required placeholder="Your Name">
                        </div>
                        <div class="input-group">
                            <input type="email" id="email" name="email" required placeholder="Your Email">
                        </div>
                    </div>
                    <div class="input-group">
                        <input type="text" id="subject" name="subject" required placeholder="Subject">
                    </div>
                    <div class="input-group">
                        <textarea id="message" name="message" required placeholder="Message"></textarea>
                    </div>
                    <button type="submit">Send Message</button>
                </form>
            </div>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>

body {
    font-family: 'Times New Roman', Times, serif;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: var(--background-color);
    color: var(--text-color);
}

:root {
    --background-color: #f0f0f0;
    --text-color: #000;
    --box-background-color: #fff;
    --box-shadow-color: rgba(0, 0, 0, 0.1);
}

body.dark-mode {
    --background-color: #121212;
    --text-color: #fff;
    --box-background-color: #1e1e1e;
    --box-shadow-color: rgba(255, 255, 255, 0.1);
}

.contact-container {
    width: 90%;
    max-width: 1200px;
    background-color: var(--box-background-color);
    box-shadow: 0 0 10px var(--box-shadow-color);
    padding: 20px;
    box-sizing: border-box;
    position: relative;
}

.mode-toggle-box {
    position: absolute;
    top: 20px;
    right: 20px;
    background-color: var(--box-background-color);
    border-radius: 50%;
    padding: 10px;
    box-shadow: 0 0 5px var(--box-shadow-color);
}

#mode-toggle {
    background: none;
    border: none;
    cursor: pointer;
}

#mode-toggle img {
    width: 30px;
    height: 30px;
}

.contact-header {
    text-align: center;
    margin-bottom: 20px;
}

.contact-content {
    display: flex;
    flex-wrap: wrap;
}

.contact-left, .contact-right {
    padding: 20px;
    box-sizing: border-box;
    flex: 1 1 50%;
}

.contact-left {
    border-right: 1px solid #ddd;
}

body.dark-mode .contact-left {
    border-right: 1px solid #444;
}

.contact-left h3 {
    text-align: center;
    margin-bottom: 10px;
}

.box {
    margin-bottom: 20px;
    padding: 20px;
    border-radius: 5px;
    background-color: var(--box-background-color);
    box-shadow: 0 0 5px var(--box-shadow-color);
}

.social-icon {
    text-align: center;
    margin-bottom: 10px;
}

.social-icon img {
    width: 30px;
    height: 30px;
}

.social-links {
    display: flex;
    justify-content: center;
    gap: 10px;
}

.social-links a img {
    width: 30px;
    height: 30px;
}

.contact-info {
    display: flex;
    justify-content: space-between;
}

.contact-info .box {
    flex: 1;
    margin-right: 10px;
}

.contact-info .box:last-child {
    margin-right: 0;
}

.contact-info h3 {
    display: flex;
    align-items: center;
    margin-bottom: 5px;
}

.contact-info h3 img {
    width: 20px;
    height: 20px;
    margin-right: 10px;
}

.contact-right form {
    display: flex;
    flex-direction: column;
}

.input-row {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}

.input-group {
    margin-bottom: 15px;
    flex: 1 1 calc(50% - 10px);
}

.input-group:last-child {
    margin-right: 0;
}

.input-group input, .input-group textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 14px;
    box-sizing: border-box;
    background-color: var(--box-background-color);
    color: var(--text-color);
}

.input-group input::placeholder, .input-group textarea::placeholder {
    font-size: 12px;
    color: #aaa;
}

body.dark-mode .input-group input, body.dark-mode .input-group textarea {
    border: 1px solid #444;
}

textarea {
    height: 100px;
    resize: none;
}

button {
    padding: 10px 15px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background-color: #0056b3;
}

/* Media Queries for Responsive Design */

/* Tablets in portrait mode */
@media (max-width: 1024px) {
    .contact-content {
        flex-direction: column;
    }

    .contact-left, .contact-right {
        flex: 1 1 100%;
        border-right: none;
        border-bottom: 1px solid #ddd;
    }

    body.dark-mode .contact-left, body.dark-mode .contact-right {
        border-bottom: 1px solid #444;
    }

    .contact-right {
        border-bottom: none;
    }

    .input-row {
        flex-direction: column;
    }

    .input-group {
        flex: 1 1 100%;
        margin-right: 0;
    }

    .contact-info {
        flex-direction: row;
        justify-content: space-between;
    }

    .contact-info .box {
        flex: 1 1 calc(50% - 10px);
        margin-right: 10px;
        margin-bottom: 0;
    }

    .contact-info .box:last-child {
        margin-right: 0;
    }
}

/* Mobile devices */
@media (max-width: 768px) {
    .contact-content {
        flex-direction: column;
    }

    .contact-left, .contact-right {
        flex: 1 1 100%;
        border-right: none;
        border-bottom: 1px solid #ddd;
    }

    body.dark-mode .contact-left, body.dark-mode .contact-right {
        border-bottom: 1px solid #444;
    }

    .contact-right {
        border-bottom: none;
    }

    .input-row {
        flex-direction: column;
    }

    .input-group {
        flex: 1 1 100%;
        margin-right: 0;
    }

    .contact-info {
        flex-direction: row;
        justify-content: space-between;
    }

    .contact-info .box {
        flex: 1 1 calc(50% - 10px);
        margin-right: 10px;
        margin-bottom: 0;
    }

    .contact-info .box:last-child {
        margin-right: 0;
    }

    .social-links {
        flex-direction: column;
    }

    .social-links a {
        margin-bottom: 10px;
    }
}

/* Small mobile devices */
@media (max-width: 480px) {
    .contact-container {
        width: 95%;
        padding: 10px;
    }

    .box {
        padding: 15px;
    }

    .social-icon img {
        width: 25px;
        height: 25px;
    }

    .social-links a img {
        width: 25px;
        height: 25px;
    }

    .contact-info h3 img {
        width: 15px;
        height: 15px;
    }

    button {
        padding: 8px 12px;
        font-size: 14px;
    }
}
document.getElementById('mode-toggle').addEventListener('click', () => {
    document.body.classList.toggle('dark-mode');
});

Note: link with html 
