# Gemini 2.0 Flash Multimodal Live API Client with RoArm-M2 Robotic Arm Integration (Vanilla JS)

This project is a web application that demonstrates the capabilities of the Gemini 2.0 Flash Multimodal Live API, enhanced with control over a RoArm-M2 robotic arm. It allows users to interact with the API using text, audio, video, and screen sharing in real-time, and to command a RoArm-M2 robotic arm through function calling.

## Features

* **Text Input:** Send text messages to the Gemini API and receive responses.
* **Audio Input:** Use your microphone to send audio input to the API.
* **Audio Output:** Hear the API's responses through your speakers.
* **Video Input:** Send video from your webcam to the API. (It uses motion detection to aviod sending static frames for better performance)
* **Screen Sharing:** Share your screen with the API.
* **Real-time Interaction:** Experience low-latency interactions with the API made possible by optimizations.
* **Function Calling:** Utilize function calling capabilities for enhanced interactions.
* **RoArm-M2 Robotic Arm Control:** Control a RoArm-M2 robotic arm using function calls.
* **Visual Feedback:** Audio visualizers provide real-time feedback on audio input and output levels.
* **Error Handling:** Robust error handling and logging for debugging.

## Getting Started

### Prerequisites

* A modern web browser that supports the Web Audio API, WebRTC, and WebSockets.
* A Google AI Studio API key.
* Python 3.0 or higher.
* A RoArm-M2 robotic arm (optional, for robotic arm control).

### Main Web Interface Installation

1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Create a `config.js` file inside the `js/config` directory.
4. Add your Google AI Studio API key to `config.js` following the instructions in `js/config/README.md`.
5. Run `python -m http.server` in the project root. (It runs at `localhost:8000` by default but you can just write a port after like `python -m http.server 3000` to run it at `localhost:3000`)

### RoArm-M2 Installation

1. Enable STA mode on the RoArm-M2 and get the IP address that will be displayed on the OLED screen (read mode in [RoArm-M2-S_WIFI_Configuration](https://www.waveshare.com/wiki/RoArm-M2-S_WIFI_Configuration))
2. Add the IP address to the `config.js` file in the `js/config` directory.

### Usage

1. Click the "Connect" button to establish a connection to the Gemini API.
2. Enter text messages in the input field and click "Send" to interact with the API.
3. Click the microphone button to start sending audio input.
4. Click the camera button to start sending video from your webcam.
5. Click the screen share button to share your screen.
6. To control the RoArm-M2, use specific commands that trigger the `pickUp` and `putDown` functions. Refer to the `js/tools/ro-arm.js` for details on the available commands.
7. Observe the logs in the logs container for real-time updates and debugging information.

## Project Structure

The project is organized into several directories:

* `js/`: Contains the JavaScript code for the application.
* `audio/`: Handles audio input, output, and processing.
* `config/`: Contains configuration file, including API keys and settings.
* `core/`: Implements core functionalities like the WebSocket client and worklet registry.
* `tools/`: Defines tools for function calling with the Gemini API. You can add your own tools here. Read more in `js/tools/README.md`
* `tools/ro-arm.js`: Implements the RoArm-M2 robotic arm control tool.
* `utils/`: Provides utility functions for logging, error handling, and data conversion.
* `video/`: Manages video input and screen sharing.
* `css/`: Contains the CSS stylesheet for the application.

## Important Notes

* Ensure that your API key is kept secure and not exposed publicly (add `config.js` to `.gitignore`).
* Refer to the `js/config/README.md` file for detailed instructions on configuring your API key.
* The application is designed for modern web browsers and may not be compatible with older browsers.
* The RoArm-M2 control is an optional feature and requires a physical RoArm-M2 device to function.

## Contributing

Contributions to this project are welcome. Please feel free to submit pull requests or open issues on the repository.

## License

This project is licensed under the MIT License.
