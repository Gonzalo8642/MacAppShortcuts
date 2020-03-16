# How to use keyboard shortcuts to open applications on MacOS

## Step 1: Create an AppleScript to open the application

- Open "Automator" (prebuilt into all macs)

- Select "New Document" if it doesn't propt you to select a document type

- Select "Quick Action" like the image below

  ![Screen Shot 2020-03-15 at 9.04.52 PM](macAppShortcuts.assets/Screen Shot 2020-03-15 at 9.04.52 PM-4325590.png)

- Enter "no input" into the drop down for `Workflow receives Automatic (text) in any appication`
- Search for "apple" to sort all the different actions. 
- Find and drag "Run AppleScript" into the right side where it says `Drag actiosn or files here to build your workflow`. See below image

![Screen Shot 2020-03-15 at 9.10.36 PM](../Library/Application Support/typora-user-images/Screen Shot 2020-03-15 at 9.10.36 PM.png)

- Paste the below code as the AppleScript, replace the `Terminal` with the application name

- ```bash
  on run {input, parameters}
  	tell application "Terminal"
  		activate
  	end tell
  end run
  ```

- Hit CMD + S to save. Give it a name (Open Terminal)



## Step 2 ) Create shortcut

- Open prefrences 
  - Apple Icon at the top right  > System Preferences
- Go to keyboard shortcuts
  - Keyboard > Shortcuts tab > Services in left side
  - Scroll down under General to see your service (Open Terminal)
- Click "Add Shortcut" to add your shortcut

![Screen Shot 2020-03-15 at 9.17.26 PM](macAppShortcuts.assets/Screen Shot 2020-03-15 at 9.17.26 PM-4325640.png)

- Make sure not to pick a shortcut that is used by Mac OS such as CMD + SPACE
