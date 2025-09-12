# Live Preview AR Code Editor

A web-based code editor that allows users to write HTML, CSS, and JavaScript code with real-time preview functionality. The editor includes mobile-friendly ad integration with features like ad rotation, ad load failure handling, and user-controlled ad dismissal.

## Features

- **Real-Time Code Preview**: Write HTML, CSS, and JavaScript code in separate tabs and see the output instantly in a preview pane.
- **Mobile-Friendly Ads**: Displays two mobile-friendly ad formats (300x250 and 320x50) within a designated ad container.
- **Ad Rotation**: Automatically rotates ads every 10 seconds, displaying one ad at a time.
- **Ad Load Failure Handling**: If an ad fails to load, the specific ad unit is hidden. If all ads fail, the entire ad container is hidden.
- **User-Controlled Ad Dismissal**: Each ad includes a close button ('X') for users to dismiss individual ads.
- **Responsive Design**: Optimized for both desktop and mobile devices, with smaller ad formats prioritized on screens smaller than 400px.
- **No Auto-Save**: Code is not saved automatically, ensuring a fresh start on page refresh.
- **Ad Placeholder in Preview**: Ads written in the HTML code (e.g., `<ins>` or `.adsbygoogle`) are displayed as placeholders in the preview pane.
- **Welcome Message**: Displays a welcome message on page load to guide users.

## Prerequisites

- A modern web browser (e.g., Chrome, Firefox, Safari, Edge).
- Internet connection for loading external ad scripts.
- A text editor or IDE to modify the code (optional).

## Installation

1. **Clone or Download the Repository**:
   ```bash
   git clone <repository-url>



Alternatively, download the project files as a ZIP and extract them.
Open the Project:
Navigate to the project directory.
Open the index.html file in a web browser to run the application.
Ensure Internet Connectivity:
The ad scripts require an internet connection to load ads from highperformanceformat.com.
Usage
Open the Editor:
Open index.html in a web browser.
A welcome message will appear: "Welcome to Live Preview AR! Start coding in HTML, CSS, or JavaScript and see the results below."
Write Code:
Use the tabs to switch between HTML, CSS, and JavaScript editors.
Write or edit code in the respective textarea fields.
The preview pane below the editor updates in real-time to reflect your changes.
Ad Integration:
Ads (300x250 or 320x50) are displayed in the designated ad container at the bottom.
Only one ad is shown at a time, rotating every 10 seconds.
On screens smaller than 400px, only the 320x50 ad is displayed.
If an ad fails to load, it is hidden, and the ad container is hidden if all ads fail.
Click the 'X' button on an ad to dismiss it. If all ads are dismissed, the ad container is hidden.
Preview Ads:
If your HTML code includes <ins> tags or .adsbygoogle classes, they will appear as placeholders in the preview pane.
Note:
Code is not saved; refreshing the page resets to the default code.
Project Structure
├── index.html       # Main HTML file containing the editor and ad integration
└── README.md        # Project documentation
Ad Integration Details
Ad Formats:
300x250 (Mobile-friendly)
320x50 (Mobile-friendly)
Ad Source: Ads are loaded from highperformanceformat.com using provided script keys.
Ad Container:
Ads are confined within the .ad-container element using overflow: hidden, max-width: 320px, and max-height: 250px to prevent overflow.
The container is hidden by default and shown only when an ad loads successfully.
Ad Rotation:
Ads rotate every 10 seconds, selecting a random ad from available (non-dismissed or non-failed) ad units.
Close Button:
Each ad has an 'X' button for dismissal, styled with a red circular background.
Error Handling:
If an ad script fails to load, the specific ad unit is hidden.
If all ads fail or are dismissed, the entire ad container is hidden.
Troubleshooting
Ads Not Loading:
Ensure you have an active internet connection.
Verify the ad script URLs and keys in the index.html file.
Check the browser console for errors related to ad scripts.
"handleAdError is not defined" Error:
This issue has been fixed by defining the handleAdError() function before ad scripts are loaded.
Ads Overflowing:
The .ad-container and .ad-unit elements use overflow: hidden and size constraints to prevent ads from exceeding their designated area.
Preview Ads Not Showing:
Real ad scripts may not load in the <iframe> preview due to browser security restrictions. Placeholders are used for <ins> and .adsbygoogle elements.
Customization
Change Ad Rotation Interval:
Modify the setInterval(rotateAds, 10000) value in the <script> section to adjust the rotation time (in milliseconds).
Ad Styling:
Edit the .ad-container, .ad-unit, or .close-ad CSS classes to customize ad appearance or close button styling.
Welcome Message:
Replace the alert() in the window.onload function with a custom modal or toast notification for a better user experience.
Add Syntax Highlighting:
Integrate libraries like CodeMirror or Prism.js for colored syntax highlighting in the editor.
Contributing
Contributions are welcome! Please follow these steps:
Fork the repository.
Create a new branch for your feature or bug fix.
Submit a pull request with a detailed description of your changes.
License
This project is licensed under the MIT License. See the LICENSE file for details.