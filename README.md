<div id="top"></div>

<!-- PROJECT LOGO -->
<br />
<div align="center">

  <h1 align="center">Post Automations</h1>

  <p align="center">
    DaVinci Resolve + Automator
  </p>
</div>

<!-- ABOUT -->
## About

Post Automations allows you to run MacOS Automator Actions and Workflows from the Delivery Page of Blackmagic Design's DaVinci Resolve.

It includes an example Automator Workflow called "send_message" that will send an iMessage to the "Home Phone Number" of the current logged in user. Be advised: If the "Home Phone Number" is the same number that you are sending the message from you will see message duplicates in iMessage because you sent the message to yourself.

### Built With
* [python](https://python.org/)
* [Automator](https://support.apple.com/guide/automator/welcome/mac)

### Compatibility
This only works on MacOS, and I have only tested it on BigSur and Monterey.

### Installation
1. Download a copy of this repo as a ZIP. Click the green Code button at the top right of the page, then Download ZIP.
2. Extract the files into a folder.
3. Following the path names provided in the zip file, copy postcat.py into:
   ```
   /Library/Application Support/Blackmagic Design/DaVinci Resolve/Fusion/Scripts/Deliver/
   ```
4. Copy the Post Automations from Documents into "Documents".
   ```
   ~/Documents/Post Automations/
   ```

<!-- USAGE EXAMPLES -->
## Usage

### Delivery Page Setup:

1. Open the the Delivery Page of Resolve.
2. In the Render Settings (left panel) scroll to "Advanced Settings".
3. Select the checkbox for "Trigger Script at: and select "End".
4. Select "postcat" from the Script dropdown menu directly below.
5. If you save a preset template, this will always run when using the template. Otherwise you will need to add the postcat trigger script manually whenever you set up a Render Job in a New Project.

### Automator Setup:

1. Open Contacts and set "Home Phone Number" for the currently logged in user to your iMessage phone number if it is not set.
2. Launch a very short Render Job as a test and MacOS will ask for various permissions. You need to do this step one time to give permissions to Automator.
3. When the job is complete you should receive an iMessage.

<!-- EDITING AUTOMATIONS AND WORKFLOWS -->
## Editing Automations and Workflows
Hopefully you already know how to use Automator. If not, please check out this how-to video https://www.youtube.com/watch?v=BTmZOh1GI3U.

### Create a new Workflow
1. Open Automator.
2. Select File > New.
3. Select "Workflow".
4. Create your Workflow and save it inside the Post Automations directory.

### Editing the Launcher
1. Select File > Open.
2. Navigate to Documents/Post Automations.
3. Select the Launcher to open it inside Automator.
4. You will see the send_message Workflow is already added to the Launcher.
5. Optional: If you like, delete the send_message Workflow.
6. To add your new Workflow, drag it into Automator from the Post Automations directory.
7. Tip: Automations will run in order. If you leave the send_message Workflow, place it at the bottom so it runs last once all other Workflows are complete.
8. Select File > Save or CMD+S to save the Launcher config.

<!-- LICENSE -->
## License

Distributed under the Apache License. See `LICENSE.txt` for more information.

<!-- CONTACT -->
## Contact

pressreset - [@pressreset](https://twitter.com/pressreset)

Project Link: [https://github.com/pressreset/Post-Automations](https://github.com/pressreset/Post-Automations)
