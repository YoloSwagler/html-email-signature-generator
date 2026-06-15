# html-email-signature-generator
A lightweight, self-contained HTML/CSS/JavaScript email signature generator for creating standardized full and reply email signatures.



# Email Signature Generator

A lightweight, self-contained, vibe coded email signature generator built with HTML, CSS, and vanilla JavaScript.

This project allows an organization to create a hidden or internal webpage where employees can enter their information and generate standardized email signatures. The page outputs both a full signature and a shorter reply signature that can be copied and pasted into Outlook or another email client.

## Features

* Self-contained HTML, CSS, and JavaScript
* No database required
* No build process required
* No external JavaScript libraries required
* Generates a full email signature
* Generates a shorter reply signature
* Copy-to-clipboard buttons
* Optional branded image or themed graphic
* Phone number formatting
* Required fields for consistent output
* Location dropdown support
* Custom location option
* Help article section for signature setup instructions
* Table-based signature layout for better Outlook compatibility
* Inline styles in the generated signature HTML for better email client support

## How It Works

The page includes a form where users enter their information. JavaScript reads the form values and dynamically builds the email signature preview.

When the user clicks a copy button, the generator copies the formatted HTML signature to the clipboard. The user can then paste it into their email client’s signature settings.

The signature output uses table-based HTML and inline styles because those are generally more reliable in email clients than modern layout methods like flexbox or grid.

## Basic Installation

1. Download or copy the HTML file.
2. Upload it to your website, intranet, or internal resource page.
3. Update the organization-specific information in the HTML and JavaScript.
4. Update the branded image URL if using a logo, campaign graphic, or theme image.
5. Test the generated signature in your email client.
6. Share the page link with employees or internal users.

## Customization

You will likely want to customize the following:

* Organization name
* Website URL
* Brand colors
* Logo or theme image
* Address options
* Phone number examples
* Help article links
* Default sample data
* Required fields
* Signature layout
* Signature text styling

## Theme Image / Logo

If your full signature includes an image, the image should be hosted at a public HTTPS URL.

For example:

https://www.example.edu/path-to-your-signature-image.png

Then update the image URL in the JavaScript:

var THEME_IMAGE_URL = "https://www.example.edu/path-to-your-signature-image.png";

Using a public image URL worked for me.. I don't know if that is the ideal long term solution however..

Important: Some email clients may still block remote images by default depending on the recipient’s email settings.

## Outlook Compatibility

This generator is designed with Outlook compatibility in mind. The generated signature uses tables and inline styles because Outlook does not always support modern HTML and CSS consistently inside email signatures.

For best results, test the signature in:

* Outlook on the web
* New Outlook for Windows
* Classic Outlook for Windows
* Outlook for Mac
* Outlook mobile app

## Limitations

This project does not centrally manage email signatures. It creates copy-and-paste signatures for users.

That means each user is responsible for adding the generated signature to their own email client.

This project also does not automatically sync signatures across devices. A user may need to add the signature separately in multiple Outlook environments.

## File Structure

This project can be used as a single HTML file.

Example:

email-signature-generator.html

If desired, the CSS and JavaScript can also be separated into their own files:

index.html
style.css
script.js

However, the single-file version may prove useful for CMS pages where everything needs to live in one page body.

## Credits

This was vibe coded and then tweaked for my specific use case. Do with it what you will. lol
