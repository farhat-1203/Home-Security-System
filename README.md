# Home Security System

A Python-based home security system that utilizes motion detection and sends an email alert with an attached image of the detected motion. This project is designed to enhance home safety by notifying the user whenever an intrusion is detected.

## Features

1. **Motion Detection**: The system uses OpenCV to detect motion via a webcam or connected camera.
2. **Email Alerts**: Once motion is detected, the system captures a frame of the motion and sends it as an email attachment to the predefined recipient.

## Requirements

Ensure you have the following installed on your system:

- Python 3.10 or later
- OpenCV (`cv2`)
- smtplib for sending emails
- NumPy (`numpy`)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/farhat-1203/Home-Security-System.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Home-Security
   ```
3. Install the required libraries:
   ```bash
   pip install opencv-python numpy
   ```

## Usage

1. Open the `send_mail.py` file and configure the following variables:
   - `gmail_user`: Your Gmail address
   - `gmail_password`: Your app-specific password
   - `to`: The recipient's email address

   **Note**: Ensure you've enabled app-specific passwords in your Google account settings.

2. Run the `detector.py` file to start the security system:
   ```bash
   python detector.py
   ```

3. The system will begin detecting motion. If motion is detected, an email with the captured frame will be sent to the specified recipient.

## Project Structure

```
Home-Security/
|-- detector.py        # Main script for motion detection
|-- send_mail.py       # Script for sending email alerts
|-- requirements.txt   # Required libraries
|-- README.md          # Project documentation
```

## How It Works

1. **Motion Detection**: The system uses OpenCV to compare consecutive video frames to identify changes, which are interpreted as motion.
2. **Email Alerts**: When motion is detected, the `send_mail.py` script is called to send an email to the predefined recipient with the captured frame as an attachment.

## Limitations

- Requires the system to remain active for continuous monitoring.
- Only supports email notifications for now (no push notifications or app integration).
- The motion detection is sensitive to environmental changes, such as lighting.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- OpenCV documentation for providing useful resources for motion detection.
- Python community for libraries and support.
