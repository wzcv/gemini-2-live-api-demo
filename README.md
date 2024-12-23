# Gemini 2.0 Flash Multimodal Live API Client written in vanilla JS

This project is a web application that demonstrates the capabilities of the Gemini 2.0 Flash Multimodal Live API. It allows users to interact with the API using text, audio, video, and screen sharing in real-time. 
Made possible by [Google's original React based repository](https://github.com/google-gemini/multimodal-live-api-web-console).

> **Note:** You're currently viewing the GitHub Pages branch. For local development, please switch to the `main` branch.

## Inspiration

This repository was inspired by [this issue](https://github.com/google-gemini/multimodal-live-api-web-console/issues/19)

It aims to demonstrate the Gemini 2.0 Flash Multimodal Live API using a simple web client built with vanilla JavaScript, HTML, and CSS. It was created to address the complexity of the original React-based implementation found in the [Google's original React based repository](https://github.com/google-gemini/multimodal-live-api-web-console). The original implementation, while functional, introduced unnecessary dependencies and a build process that obscured the simplicity of interacting with the API. This project simplifies the development process by removing the need for React, TypeScript, SCSS, and a complex build chain, making it more accessible and easier to understand for a wider range of developers.

## Demo

You can try out the live demo at: [GitHub Pages Demo Link]

## Features

*   **Text Input:** Send text messages to the Gemini API and receive responses.
*   **Audio Input:** Use your microphone to send audio input to the API.
*   **Audio Output:** Hear the API's responses through your speakers.
*   **Video Input:** Send video from your webcam to the API. (It uses motion detection to aviod sending static frames for better performance)
*   **Screen Sharing:** Share your screen with the API.
*   **Real-time Interaction:** Experience low-latency interactions with the API made possible by optimizations.
*   **Function Calling:** Utilize function calling capabilities for enhanced interactions.
*   **Visual Feedback:** Audio visualizers provide real-time feedback on audio input and output levels.
*   **Error Handling:** Robust error handling and logging for debugging.

## Getting Started

### Prerequisites

*   A modern web browser that supports the Web Audio API, WebRTC, and WebSockets.
*   A Google AI Studio API key.
*   For local development:
    *   Python 3.0 or higher (for running a local server)
    *   OR any other local development server of your choice (e.g., Live Server VS Code extension)

### Installation

#### Local Development
1. Switch to the `main` branch
2. Clone this repository to your local machine
3. Navigate to the project directory
4. Create a `config.js` file inside the `js/config` directory
5. Add your Google AI Studio API key to `config.js` following the instructions in `js/config/README.md`
6. Start a local server:
   * Using Python: `python -m http.server` (defaults to `localhost:8000`)
   * Or use any other local development server

#### Using GitHub Pages Version
1. Visit the live demo link
2. Enter your API key in the configuration panel
3. Start using the application

### Usage

1. Click the "Connect" button to establish a connection to the Gemini API.
2. Enter text messages in the input field and click "Send" to interact with the API.
3. Click the microphone button to start sending audio input.
4. Click the camera button to start sending video from your webcam.
5. Click the screen share button to share your screen.
6. Observe the logs in the logs container for real-time updates and debugging information.

## Project Structure

The project is organized into several directories:

*   `js/`: Contains the JavaScript code for the application.
    *   `audio/`: Handles audio input, output, and processing.
    *   `config/`: Contains configuration file, including API keys and settings.
    *   `core/`: Implements core functionalities like the WebSocket client and worklet registry.
    *   `tools/`: Defines tools for function calling with the Gemini API. You can add your own tools here. Read more in `js/tools/README.md`
    *   `utils/`: Provides utility functions for logging, error handling, and data conversion.
    *   `video/`: Manages video input and screen sharing.
*   `css/`: Contains the CSS stylesheet for the application.

## Security Considerations

*   The GitHub Pages version stores your API key in browser localStorage for convenience
*   For production use, it's recommended to use the local development version and keep your API key secure
*   Never commit your `config.js` file containing your API key to version control
*   Consider implementing proper backend authentication for production deployments

## Important Notes

*   This branch is specifically configured for GitHub Pages hosting
*   For local development, please use the `main` branch
*   Ensure that your API key is kept secure and not exposed publicly
*   The application requires modern web browser features and may not work in older browsers

## Contributing

Contributions to this project are welcome. Please feel free to submit pull requests or open issues on the repository.

## License

This project is licensed under the MIT License.
