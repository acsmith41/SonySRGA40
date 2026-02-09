# SonySRGA40
Qsys control module for a Sony SRGA40 PTZ Camera

To use the QSYS plugin, download the file and move it to your QSC/Q-Sys Designer/Plugins folder.
<br>This plugin is intended to be used with a camera that has its SSL setting 'enabled.' Testing was performed with a self-signed certificate.
<br>If you need to disable SSL on the camera, change the command strings in this module with "https..." to "http..."

Controls:
<br><br>
  &ensp;Text (user input):<br>
    &ensp;&ensp;Ip:
     <br>&ensp;&ensp;&ensp;The camera's IP address.<br>
    &ensp;&ensp;Username:
      <br>&ensp;&ensp;&ensp;The camera's username.<br>
    &ensp;&ensp;Password:
      <br>&ensp;&ensp;&ensp;The camera's password.<br>
    &ensp;&ensp;PollTime:
      <br>&ensp;&ensp;&ensp;The module will convert this text input to a number, and poll the camera's status once every {PollTime} seconds.<br>
      <br>
   &ensp;Power:<br>
    &ensp;&ensp;PowerToggle:
      <br>&ensp;&ensp;&ensp;Press to toggle camera's power mode (if camera is on, pressing toggle will put camera in Standby mode).<br>
    &ensp;&ensp;PowerOn:
      <br>&ensp;&ensp;&ensp;Trigger to turn camera on.<br>
    &ensp;&ensp;PowerOff:
      <br>&ensp;&ensp;&ensp;Trigger to put camera into 'Standby' mode.<br>
    &ensp;&ensp;PowerReboot:
      <br>&ensp;&ensp;&ensp;Press or trigger to power cycle camera.<br>
      <br>
   &ensp;PTZ:<br>
    &ensp;&ensp;PanLeft:
      <br>&ensp;&ensp;&ensp;Press (and hold) to pan camera left.
       <br>&ensp;&ensp;&ensp;('left' being from the camera's perspective, when camera is sitting on a table - if camera is mounted 'upside-down,' camera will pan right)<br>
    &ensp;&ensp;PanRight:
      <br>&ensp;&ensp;&ensp;Press (and hold) to pan camera right.<br>
    &ensp;&ensp;TiltUp:
      <br>&ensp;&ensp;&ensp;Press (and hold) to tilt camera up.<br>
    &ensp;&ensp;TiltDown:
      <br>&ensp;&ensp;&ensp;Press (and hold) to tilt camera down.<br>
    &ensp;&ensp;UpLeft:
      <br>&ensp;&ensp;&ensp;Press (and hold) to tilt camera up and pan camera left.<br>
    &ensp;&ensp;UpRight:
      <br>&ensp;&ensp;&ensp;Press (and hold) to tilt camera up and pan camera right.<br>
    &ensp;&ensp;DownLeft:
      <br>&ensp;&ensp;&ensp;Press (and hold) to tilt camera down and pan camera left.<br>
    &ensp;&ensp;DownRight:
      <br>&ensp;&ensp;&ensp;Press (and hold) to tilt camera down and pan camera right.<br>
    &ensp;&ensp;ZoomIn:
      <br>&ensp;&ensp;&ensp;Press (and hold) to zoom camera in.<br>
    &ensp;&ensp;ZoomOut:
      <br>&ensp;&ensp;&ensp;Press (and hold) to zoom camera out.<br>
      <br>      
   &ensp;PresetCoords:
    <br>&ensp;&ensp;PresetRecall [1-5]:
      <br>&ensp;&ensp;&ensp;Press (less than 2 seconds) to recall camera to corresponding preset PTZ values.
      <br>&ensp;&ensp;&ensp;Hold (2 seconds or longer) to store current PTZ values to corresponding preset.<br>
    &ensp;&ensp;PresetStore [1-5]:
      <br>&ensp;&ensp;&ensp;Press to store camera's current PTZ values to corresponding preset.<br>
    &ensp;&ensp;Home:
      <br>&ensp;&ensp;&ensp;Returns the camera to the home location stored on the camera (use camera's web interface to set home position).<br>
    &ensp;&ensp;Privacy:
      <br>&ensp;&ensp;&ensp;Privacy turns the camera to [2200,0000]. The camera had trouble leaving a true 180 degree facing, so this is slightly offset.<br>
      <br>
   &ensp;AutoframingMultitracking:
    <br>&ensp;&ensp;AutoframeToggle:
      <br>&ensp;&ensp;&ensp;Press to toggle the state of the camera's Autoframing function (if Autoframing is on, pressing this will turn Autoframing off).<br>
    &ensp;&ensp;MultitrackingToggle:
      <br>&ensp;&ensp;&ensp;Press to toggle the state of the camera's function that directs the camera to track multiple targets.
      <br>&ensp;&ensp;&ensp;If Autoframing is turned off, MultitrackingToggle will turn on Autoframing.
      <br>&ensp;&ensp;&ensp;The camera will remember the last-selected number of targets to track in Multitracking mode.
      <br>&ensp;&ensp;&ensp;If Multitracking is off, the Autoframing feature will track 1 target.<br>
    &ensp;&ensp;Multitrack [2-8]:
      <br>&ensp;&ensp;&ensp;Press or trigger to change the number of targets that the camera will track, when Multitracking is enabled.
      <br>&ensp;&ensp;&ensp;Multitrack will *NOT* turn on Multitracking or Autoframing.
