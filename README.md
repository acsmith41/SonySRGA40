# SonySRGA40
Qsys control module for a Sony SRGA40 PTZ Camera

To use the QSYS plugin, download the file and move it to your QSC/Q-Sys Designer/Plugins folder.
<br>This plugin is intended to be used with a camera that has its SSL setting 'enabled.' Testing was performed with a self-signed certificate.
<br>If you need to disable SSL on the camera, change the command strings in this module with "https..." to "http..."

### Controls / Parameters:
#### Text (user input)
- Ip
  - The camera's IP address.
- Username
  - The camera's username.
- Password
  - The camera's password.
- PollTime
  - The module will convert this text input to a number, and poll the camera's status once every {PollTime} seconds.

#### Power
- PowerToggle
  - Press to toggle camera's power mode (if camera is on, pressing toggle will put camera in Standby mode).
- PowerOn
  - Trigger to turn camera on.
- PowerOff
  - Trigger to put camera into 'Standby' mode.
- PowerReboot
  - Press or trigger to power cycle camera.

#### PTZ
- PanLeft
  - Press (and hold) to pan camera left ('left' being from the camera's perspective, when camera is sitting on a table - if camera is mounted 'upside-down,' camera might pan right)
- PanRight
  - Press (and hold) to pan camera right.
- TiltUp
  - Press (and hold) to tilt camera up.
- TiltDown
  - Press (and hold) to tilt camera down.
- UpLeft
  - Press (and hold) to tilt camera up and pan camera left.
- UpRight
  - Press (and hold) to tilt camera up and pan camera right.
- DownLeft
  - Press (and hold) to tilt camera down and pan camera left.
- DownRight
  - Press (and hold) to tilt camera down and pan camera right.
- ZoomIn
  - Press (and hold) to zoom camera in.
- ZoomOut
  - Press (and hold) to zoom camera out.

#### PresetCoords:
- PresetRecall [1-5]
  - Press (less than 2 seconds) to recall camera to corresponding preset PTZ values.
  - Hold (2 seconds or longer) to store current PTZ values to corresponding preset.
- PresetStore [1-5]
  - Press to store camera's current PTZ values to corresponding preset.
- Home
  - Returns the camera to the home location stored on the camera (use camera's web interface to set home position).
- Privacy
  - Privacy turns the camera to [2200,0000]. The camera had trouble leaving a true 180 degree facing, so this is slightly offset.

#### AutoframingMultitracking:
- AutoframeToggle
  - Press to toggle the state of the camera's Autoframing function (if Autoframing is on, pressing this will turn Autoframing off).<br>
- MultitrackingToggle
  - Press to toggle the state of the camera's function that directs the camera to track multiple targets
  - If Autoframing is turned off, MultitrackingToggle will turn on Autoframing
  - The camera will remember the last-selected number of targets to track in Multitracking mode
  - If Multitracking is off, the Autoframing feature will track 1 target
- Multitrack [2-8]
  - Press or trigger to change the number of targets that the camera will track, when Multitracking is enabled.
  - Multitrack will *NOT* turn on Multitracking or Autoframing.
