
# YouTube Clone 🎥

A responsive YouTube Clone built with ReactJS, Vite, and the YouTube Data API. It features video search, playback, and a display of trending videos with detailed stats. React Router enables dynamic navigation, while Moment.js formats dates. This project highlights skills in React, API integration, and responsive UI design.


## Features

* Video Search: Search for videos using the YouTube Data API.
* Popular Videos: Displays the top 50 most popular videos in the US region.
* Video Player: Watch videos directly within the application.
* Channel Details: Shows channel information.
* Date Formatting: Uses the Moment.js library to display relative dates (e.g., "2 days ago").
* Responsive UI: Designed to work seamlessly across devices.



## Tech Stack

**Framework:** Reactjs,with Vite

**Routing:** React Router Dom

**Styling:** CSS Modules

**API:** YouTube Data API V3

**Utilities:** Moment.js for date formatting


## Prerequisites

* **Node.js** (latest stable version recommended)

* **VS Code** or any preferred code editor

* A YouTube Data API key (from Google Cloud Console)
## Installation

1. Clone the Repository:

```bash
  git clone https://github.com/your-username/youtube-clone.git

  cd youtube-clone

```
2. Install Vite and Set Up Project: Initialize the project using Vite: 

```bash  
  npm create vite@latest youtube-clone --template react

  cd youtube-clone

```
3. Install Dependencies: Install the necessary npm packages:

 ```bash 
   npm install react-router-dom moment
```
4. Set Up YouTube API Key:
  * Go to Google Cloud Console.
  * Create a new project named YouTubeClone.
  * Enable the YouTube Data API.
  * Generate API credentials and copy your API key.
  * Create a file src/data.js:
  
  ```javascript
  export const API_KEY = "your_api_key_here";
```
5. Run the Development Server:
```bash
npm run dev
```
6. Open your browser and navigate to:
```bash
http://localhost:5173/

```
 

## Key Implementation Details

## API Integration:
* YouTube Data API:

  * Fetches popular videos, video details, and channel information.
  * Example API call to fetch the most popular videos:
 ``` javascript
 const fetchPopularVideos = async () => {
    const response = await fetch(
    `https://www.googleapis.com/youtube/v3/videos?part=snippet,contentDetails,statistics&chart=mostPopular&regionCode=US&maxResults=50&key=${API_KEY}`
  );
  const data = await response.json();
  console.log(data);
};


```
* Date Formatting:
  * Used Moment.js to convert timestamps into relative time:
  ``` javscript
   import moment from "moment";
   const formattedDate = moment(videoDate).fromNow();



  ```
## Lessons Learned
* API Integration: Gained a better understanding of using third-party APIs like the YouTube Data API.
* React Router DOM: Implemented dynamic routing for video details and search pages.
* Styling: Improved skills in modular CSS for scalable styling.
## Future Enhancements
* User Authentication: Allow users to sign in and save playlists.
## Cintrubting
* Contributions are welcome! Fork the repo, create a feature branch, and submit a pull request