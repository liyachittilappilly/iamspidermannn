

# Spiderman Web Shooter

![Spiderman Web Shooter Demo](https://img.shields.io/badge/Status-Active-brightgreen) ![Python](https://img.shields.io/badge/Python-3.6%2B-blue) ![License](https://img.shields.io/badge/License-MIT-green)

A fun interactive application that uses hand tracking to simulate Spiderman's web-shooting ability! Make the iconic Spiderman pose with your hand and watch as web particles shoot from your wrist in real-time.

## Features

- **Hand Pose Recognition**: Detects the classic Spiderman web-shooting hand gesture
- **Real-time Visual Effects**: Generates particle effects that simulate web shooting
- **Directional Web Shooting**: Web particles shoot in the direction your middle finger points
- **Interactive Particle System**: Realistic web particles with physics simulation
- **Mirror Effect**: Flips the camera feed for intuitive interaction

## How It Works

The application uses MediaPipe's hand tracking technology to detect hand landmarks and recognize specific finger positions:

1. **Hand Detection**: MediaPipe Hands detects your hand and identifies 21 key landmarks
2. **Pose Recognition**: The system checks for:
   - Thumb and index finger touching (forming the "O" shape)
   - Middle, ring, and pinky fingers extended (pointing upward)
3. **Web Effect Generation**: When the pose is detected:
   - Web particles are created at the wrist position
   - Particles shoot in the direction of your middle finger
   - Each particle has randomized properties for realistic effect
4. **Physics Simulation**: Particles gradually slow down and fade out over time

## Installation

### Prerequisites

- Python 3.6 or higher
- A working webcam
- OpenCV-compatible system

### Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/spiderman-web-shooter.git
   cd spiderman-web-shooter
   ```

2. Install the required packages:
   ```bash
   pip install opencv-python mediapipe numpy
   ```

3. Run the application:
   ```bash
   python spiderman_web_shooter.py
   ```

## Usage

1. **Start the Application**: Run the script and position your hand in front of the camera.
2. **Make the Spiderman Pose**:
   - Touch your thumb and index finger together to form an "O"
   - Extend your middle, ring, and pinky fingers upward
3. **Aim**: Point your middle finger in the direction you want to shoot webs
4. **Watch the Magic**: Web particles will shoot from your wrist in the direction you're pointing
5. **Exit**: Press 'q' to close the application.

### Controls

| Key | Action |
|-----|--------|
| q   | Exit application |

## Requirements

- Python 3.6+
- OpenCV (cv2)
- MediaPipe
- NumPy
- A working webcam

## Technical Details

The application uses several key components:

- **Hand Landmark Detection**: MediaPipe Hands identifies 21 landmarks on each hand
- **Distance Calculation**: Measures the distance between thumb and index finger tips
- **Finger Extension Detection**: Determines if fingers are extended based on landmark positions
- **Particle System**: Creates and manages web particles with physics simulation
- **Orientation Detection**: Determines if the hand is upright or inverted

## Customization

You can adjust the following parameters in the code:

- `particle_speed`: Range of initial particle speeds (default: 10-20)
- `particle_creation_rate`: Time between particle creation (default: 0.05 seconds)
- `particle_count`: Number of particles created per burst (default: 5)
- `angle_offset`: Randomness in particle direction (default: ±0.3 radians)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [MediaPipe](https://google.github.io/mediapipe/) for the hand tracking technology
- [OpenCV](https://opencv.org/) for computer vision capabilities
- Marvel for creating the iconic Spiderman character and web-shooting pose

---

**Note**: This application uses your webcam only for local processing. No video data is transmitted or stored.
