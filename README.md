

## Extensions ##

### VS Code ###
- Out of box
- Mac: ~/.vscode/extensions
  - Cmd + Shft + P -> Shell: install 'code' in Path
- Ubuntu: Home/.vscode/extensions
- USER SETTINGS: {  
    "typescript.tsdk": "${npm list -g | head -n1}/node_modules/typescript/lib",  
    "editor.detectIndentation": false,  
    "editor.insertSpaces": true,  
    "editor.tabSize": 3,  
    "editor.fontFamily": "'Andale Mono', 'Lucida Console'",  
    "editor.fontSize": 13,  
    "editor.fontLigatures": true,  
    "git.autofetch": true,  
    "terminal.integrated.fontSize": 12,  
    "terminal.integrated.fontFamily": "Monaco",  
    "window.zoomLevel": -0.5,  
    "workbench.colorTheme": "Default Dark+",  
    "workbench.iconTheme": "material-icon-theme",  
    "javascript.validate.enable": false, // if not using TS  
    "flow.enabled": true,  
    "flow.useNPMPackagedFlow": true,  
    "flow.pathToFlow": "../node_modules/.bin/flow" // or install npm i flow-bin -g  
  }
- WORKSPACE SETTINGS: {  
    "javascript.validate.enable": false, // if not using TS  
    "flow.enabled": true,  
    "flow.useNPMPackagedFlow": true,  
    "flow.pathToFlow": "${workspaceFolder}/node_modules/.bin/flow" // or install npm i flow-bin -g  
  }

### Sublime ###
- Git  
TypeScript  
Babel ES6/ES7  
JsFormat  
BracketHighlighter  
SideBarEnhancements  
Color Highlighter  
A File Icon  
Seti_UI, Materialize, Tomorrow Color Schemes, Predawn, Monokai - Spacegray  

### Atom ###
- Atom-Typescript: https://github.com/TypeStrong/atom-typescript  
Atom-React: https://github.com/orktes/atom-react (clone into .atom\packages folder)  
Install: file-icons, atom-json-color, atom-bracket-highlight,  
Use: UITheme='One Dark', SyntaxTheme='One Light'  
Stylesheet:  
  .tree-view {  
    font-size: 10px; 
  }  
  atom-text-editor {  
    background-color: #f7f3ea;  
    font-family: Monaco;  
    font-size: 13px;  
  }  
  .bracket-matcher {  
    position: absolute;  
    top: -1px;  
    border-bottom: 1px solid lime;  
    border: 1px solid rgba(0, 255, 0, 0.7);  
    // background-color: rgba(150, 255, 150, 0.3);  
  }  

- - - -

## Boilerplates ##

### Client ###
- https://github.com/facebookincubator/create-react-app
- https://github.com/Microsoft/TypeScript-React-Starter

### Node ###
- https://github.com/Microsoft/TypeScript-Node-Starter
- https://github.com/developit/express-es6-rest-api


- - - -

# MAC #

## ~/.bash_profile ##
export CLICOLOR=1  
export LSCOLORS=ExFxBxDxCxegedabagacad  
export PATH=~/...../mongodb/bin:$PATH  
export PS1='\[\033[01;32m\]${PWD} \[\033[00m\]λ '  
alias l='ls -CF'  
alias la='ls -a'  
alias ll='ls -all'  
alias ld='ls -l'  
alias cls='clear && printf "\e[3J"'  
alias pss='ps aux | grep'  
alias mongod='mongod --dbpath ~/...../mongodb/data/db'  
eval $(/usr/libexec/path_helper -s)  

## shortcuts ##
AC2V2zZQ  
F11	=> Show desktop  
Cmd + Shift + . => show hidden files  
Cmd + Q 	=> close the application without trace  
Cmd + \`		=> tab between windows of same application  
cp -a <_source>/. <_dest> => copy the content of the <_source> into <_dest> recursively(a) including hidden files/folders(.)  
ln -s <_source> <_dest>	=> creates a link of <_source> in the <_dest> folder  
chown <_user> <_file> => changes the owner of <_file> to <_user>  
defaults write -g com.apple.mouse.scaling -float 10  

// MongoDB  
$ ./mongod --dbpath ../data/db  
$ mongo (another cmd)  
$ show dbs  
$ use <db>  
$ db  
$ show collections  
$ db.<collection>.drop()  
$ db.<collection>.insert({…})  
$ db.<collection>.find()  

// NPM  
$ sudo chown -R $(whoami) <path> | $(npm config get prefix)  

// HomeBrew . 
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"  


# UBUNTU #

## ~/.bashrc ##
'# alias l='ls -CF'  
'# alias la='ls -a'  
'# alias ll='ls -all'  
alias ld='ls -l'  
alias cls='clear && reset'  
PS1='\[\033[01;32m\]${PWD} \[\033[00m\]\$ '

## Programs ##
Gnome Tweaks, Gnome Global Application Menu, Docky (No need for Unity or Dash-to-dock),  
GIMP, VLC, K3b,  
Terminator,  
GParted, KDE Partition Manager, UNetbootin,  
https://atom.io, 

## Scripts ##
- sudo apt-get update  
- NodeJs: sudo apt-get install nodejs (may noy install the latest version)  
  curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -  
  sudo apt-get install -y nodejs  
  sudo apt-get install nodejs-legacy  
- NPM: sudo apt-get install npm  
- GIT: sudo apt-get install git  
- Chrome: sudo apt-get install google-chrome-stable
- D (ntfs):  
sudo mkdir -p /media/c  
sudo fdisk -l (ex: sda3 is our D drive)  
sudo mount -t ntfs -o nls=utf8,umask=0222 /dev/sda3 /media/c  
- if there is a problem w/ icons:  
/usr/share/pixmaps/ or /usr/share/applications/ and open related files.  
- Printer: download drivers from http://support.brother.com/g/b/producttop.aspx?c=eu_ot&lang=en&prod=dcp9055cdn_eu_as  
ipp://192.168.1.9/ipp for the URI of the wifi printer (http://localhost:631/printers for administrations)  

## Terminator ##
- Profiles -> default -> Colours -> Built-in Schemes: Gruvbox dark  
- First open terminator and set the window size according to your need and comfort.  
Right click and go to preference and then to layout.  
Click on the terminal name under window and then save the layout.  
Thats it, It will open the terminator in the same size, as you have set up, next time you open it.  
- ~home/.config/terminator/config:  
[global_config]
  suppress_multiple_term_dialog = True
  title_font = Sans 8
[keybindings]
[layouts]
  [[default]]
    [[[child0]]]
      fullscreen = False
      last_active_term = 99a44a5b-9cc5-4c49-bdc8-6cac012dcfb8
      last_active_window = True
      maximised = False
      order = 0
      parent = ""
      position = 0:0
      size = 1912, 425
      title = /bin/bash
      type = Window
    [[[terminal1]]]
      order = 0
      parent = child0
      profile = default
      type = Terminal
      uuid = 99a44a5b-9cc5-4c49-bdc8-6cac012dcfb8
[plugins]
[profiles]
  [[default]]
    background_color = "#282828"
    background_darkness = 0.95
    background_type = transparent
    copy_on_selection = True
    cursor_color = "#aaaaaa"
    cursor_shape = ibeam
    font = Monospace 9
    foreground_color = "#ffffff"
    show_titlebar = False
    use_system_font = False

## Konsole ##
~/.config/konsolerc  
[Desktop Entry]
DefaultProfile=Default.profile
[Favorite Profiles]
Favorites=
[MainWindow]
Height 1080=480
Width 1920=1298
[TabBar]
ShowQuickButtons=true
TabBarVisibility=ShowTabBarWhenNeeded

~/.local/share/konsole/Default.profile  
[Appearance]
ColorScheme=Breeze
[General]
Name=Default
Parent=FALLBACK/


## Sublime Text 3 ##
- sudo add-apt-repository ppa:webupd8team/sublime-text-3
- sudo apt-get update
- sudo apt-get install sublime-text-installer  

## Docky ##
Open gconf-editor. Navigate to */apps/docky-2/Docky/Items/DockyItem/*. Change *Hue* to 1 DockyItemCommand to *gksu nautilus /usr/share/applications*. Click on your Docky Anchor. Type in your password. Navigate to the program icon you would like to change.  


## Plasma ##

edit */usr/share/plasma/layout-templates/org.kde.plasma.desktop.defaultPanel/contents/layout.js*:  
var panel = new Panel
var panelScreen = panel.screen
var freeEdges = {"bottom": true, "top": true, "left": true, "right": true}

for (i = 0; i < panelIds.length; ++i) {
    var tmpPanel = panelById(panelIds[i])
    if (tmpPanel.screen == panelScreen) {
        // Ignore the new panel
        if (tmpPanel.id != panel.id) {
            freeEdges[tmpPanel.location] = false;
        }
    }
}

if (freeEdges["bottom"] == true) {
    panel.location = "bottom";
} else if (freeEdges["top"] == true) {
    panel.location = "top";
} else if (freeEdges["left"] == true) {
    panel.location = "left";
} else if (freeEdges["right"] == true) {
    panel.location = "right";
} else {
    // There is no free edge, so leave the default value
    panel.location = "top";
}

panel.height = gridUnit * 2

var kickoff = panel.addWidget("org.kde.plasma.kickoff")
kickoff.currentConfigGroup = ["Shortcuts"]
kickoff.writeConfig("global", "Alt+F1")

//panel.addWidget("org.kde.plasma.showActivityManager")
panel.addWidget("org.kde.plasma.pager")
panel.addWidget("org.kde.plasma.taskmanager")

/* Next up is determining whether to add the Input Method Panel
 * widget to the panel or not. This is done based on whether
 * the system locale's language id is a member of the following
 * white list of languages which are known to pull in one of
 * our supported IME backends when chosen during installation
 * of common distributions. */

var langIds = ["as",    // Assamese
               "bn",    // Bengali
               "bo",    // Tibetan
               "brx",   // Bodo
               "doi",   // Dogri
               "gu",    // Gujarati
               "hi",    // Hindi
               "ja",    // Japanese
               "kn",    // Kannada
               "ko",    // Korean
               "kok",   // Konkani
               "ks",    // Kashmiri
               "lep",   // Lepcha
               "mai",   // Maithili
               "ml",    // Malayalam
               "mni",   // Manipuri
               "mr",    // Marathi
               "ne",    // Nepali
               "or",    // Odia
               "pa",    // Punjabi
               "sa",    // Sanskrit
               "sat",   // Santali
               "sd",    // Sindhi
               "si",    // Sinhala
               "ta",    // Tamil
               "te",    // Telugu
               "th",    // Thai
               "ur",    // Urdu
               "vi",    // Vietnamese
               "zh_CN", // Simplified Chinese
               "zh_TW"] // Traditional Chinese

if (langIds.indexOf(languageId) != -1) {
    panel.addWidget("org.kde.plasma.kimpanel");
}

panel.addWidget("org.kde.plasma.systemtray")
panel.addWidget("org.kde.plasma.digitalclock")
  
  
- - - -
- - - -

# AWS #

## Installations ##
sudo apt-get update  
sudo apt-get git  
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -  
sudo apt-get install -y nodejs  
sudo apt-get install -y nodejs-legacy  
sudo apt-get install build-essential  
sudo apt-get npm  

## Deployment ##
$ ssh -i \~/.ssh/lh-accountancy-dev.pem ubuntu@ec2-35-177-20-202.eu-west-2.compute.amazonaws.com  
$ tar -cvzf lh-accountancy.tar.gz lh-accountancy  
$ scp -i \~/.ssh/lh-accountancy-dev.pem lh-accountancy.tar.gz ubuntu@ec2-35-177-20-202.eu-west-2.compute.amazonaws.com:\~  
$ sudo tar -xzvf lh-accountancy.tar.gz  
$ npm run build-dev (export NODE_ENV=dev)  
$ npm run publish-dev > ../lh-accountancy.log 2>&1 &  
$ nohup node ./lh-accountancy/dist/src/index.js > lh-accountancy.log 2>&1 &  
  
  
- - - -
- - - -

# COMMON #

## Git ##
$ git config credential.helper store  
$ git push http://example.com/repo.git  
Username: <type your username>  
Password: <type your password>  
  
  
## iTerm2 ##
{
"Profiles": [
{
  "Ansi 3 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0
  },
  "Tags" : [

  ],
  "Ansi 12 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 1
  },
  "Normal Font" : "Monaco 12",
  "Ansi 2 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Bold Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Right Option Key Sends" : 0,
  "Ansi 6 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0,
    "Blue Component" : 0.73333334922790527
  },
  "Rows" : 25,
  "Default Bookmark" : "No",
  "Non-ASCII Anti Aliased" : true,
  "Use Bright Bold" : true,
  "Ansi 10 Color" : {
    "Green Component" : 1,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 0.3333333432674408
  },
  "Ambiguous Double Width" : false,
  "Jobs to Ignore" : [
    "rlogin",
    "ssh",
    "slogin",
    "telnet"
  ],
  "Ansi 15 Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Foreground Color" : {
    "Red Component" : 1,
    "Color Space" : "sRGB",
    "Blue Component" : 1,
    "Alpha Component" : 1,
    "Green Component" : 1
  },
  "Working Directory" : "\/Users\/ayaliz01",
  "Blinking Cursor" : true,
  "Disable Window Resizing" : true,
  "Sync Title" : false,
  "Prompt Before Closing 2" : false,
  "BM Growl" : true,
  "Command" : "",
  "Description" : "Default",
  "Mouse Reporting" : true,
  "Screen" : -1,
  "Selection Color" : {
    "Green Component" : 0.8353000283241272,
    "Red Component" : 0.70980000495910645,
    "Blue Component" : 1
  },
  "Columns" : 130,
  "Idle Code" : 0,
  "Ansi 13 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Custom Command" : "No",
  "ASCII Anti Aliased" : true,
  "Non Ascii Font" : "Monaco 12",
  "Vertical Spacing" : 1,
  "Use Bold Font" : true,
  "Option Key Sends" : 0,
  "Selected Text Color" : {
    "Green Component" : 0,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Background Color" : {
    "Red Component" : 0.20000000000000001,
    "Color Space" : "sRGB",
    "Blue Component" : 0.20000000000000001,
    "Alpha Component" : 1,
    "Green Component" : 0.20000000000000001
  },
  "Character Encoding" : 4,
  "Ansi 11 Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 0.3333333432674408
  },
  "Use Italic Font" : true,
  "Unlimited Scrollback" : false,
  "Keyboard Map" : {
    "0xf700-0x260000" : {
      "Text" : "[1;6A",
      "Action" : 10
    },
    "0x37-0x40000" : {
      "Text" : "0x1f",
      "Action" : 11
    },
    "0x32-0x40000" : {
      "Text" : "0x00",
      "Action" : 11
    },
    "0xf709-0x20000" : {
      "Text" : "[17;2~",
      "Action" : 10
    },
    "0xf70c-0x20000" : {
      "Text" : "[20;2~",
      "Action" : 10
    },
    "0xf729-0x20000" : {
      "Text" : "[1;2H",
      "Action" : 10
    },
    "0xf72b-0x40000" : {
      "Text" : "[1;5F",
      "Action" : 10
    },
    "0xf705-0x20000" : {
      "Text" : "[1;2Q",
      "Action" : 10
    },
    "0xf703-0x260000" : {
      "Text" : "[1;6C",
      "Action" : 10
    },
    "0xf700-0x220000" : {
      "Text" : "[1;2A",
      "Action" : 10
    },
    "0xf701-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x42",
      "Action" : 11
    },
    "0x38-0x40000" : {
      "Text" : "0x7f",
      "Action" : 11
    },
    "0x33-0x40000" : {
      "Text" : "0x1b",
      "Action" : 11
    },
    "0xf703-0x220000" : {
      "Text" : "[1;2C",
      "Action" : 10
    },
    "0xf701-0x240000" : {
      "Text" : "[1;5B",
      "Action" : 10
    },
    "0xf70d-0x20000" : {
      "Text" : "[21;2~",
      "Action" : 10
    },
    "0xf702-0x260000" : {
      "Text" : "[1;6D",
      "Action" : 10
    },
    "0xf729-0x40000" : {
      "Text" : "[1;5H",
      "Action" : 10
    },
    "0xf706-0x20000" : {
      "Text" : "[1;2R",
      "Action" : 10
    },
    "0x34-0x40000" : {
      "Text" : "0x1c",
      "Action" : 11
    },
    "0xf700-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x41",
      "Action" : 11
    },
    "0x2d-0x40000" : {
      "Text" : "0x1f",
      "Action" : 11
    },
    "0xf70e-0x20000" : {
      "Text" : "[23;2~",
      "Action" : 10
    },
    "0xf702-0x220000" : {
      "Text" : "[1;2D",
      "Action" : 10
    },
    "0xf703-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x43",
      "Action" : 11
    },
    "0xf700-0x240000" : {
      "Text" : "[1;5A",
      "Action" : 10
    },
    "0xf707-0x20000" : {
      "Text" : "[1;2S",
      "Action" : 10
    },
    "0xf70a-0x20000" : {
      "Text" : "[18;2~",
      "Action" : 10
    },
    "0x35-0x40000" : {
      "Text" : "0x1d",
      "Action" : 11
    },
    "0xf70f-0x20000" : {
      "Text" : "[24;2~",
      "Action" : 10
    },
    "0xf703-0x240000" : {
      "Text" : "[1;5C",
      "Action" : 10
    },
    "0xf701-0x260000" : {
      "Text" : "[1;6B",
      "Action" : 10
    },
    "0xf702-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x44",
      "Action" : 11
    },
    "0xf72b-0x20000" : {
      "Text" : "[1;2F",
      "Action" : 10
    },
    "0x36-0x40000" : {
      "Text" : "0x1e",
      "Action" : 11
    },
    "0xf708-0x20000" : {
      "Text" : "[15;2~",
      "Action" : 10
    },
    "0xf701-0x220000" : {
      "Text" : "[1;2B",
      "Action" : 10
    },
    "0xf70b-0x20000" : {
      "Text" : "[19;2~",
      "Action" : 10
    },
    "0xf702-0x240000" : {
      "Text" : "[1;5D",
      "Action" : 10
    },
    "0xf704-0x20000" : {
      "Text" : "[1;2P",
      "Action" : 10
    }
  },
  "Window Type" : 0,
  "Cursor Type" : 1,
  "Background Image Location" : "",
  "Blur" : false,
  "Scrollback Lines" : 1000,
  "Send Code When Idle" : false,
  "Close Sessions On End" : true,
  "Terminal Type" : "xterm-256color",
  "Visual Bell" : true,
  "Flashing Bell" : false,
  "Silence Bell" : false,
  "Ansi 14 Color" : {
    "Green Component" : 1,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 1
  },
  "Name" : "Default",
  "Cursor Text Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Shortcut" : "",
  "Cursor Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0.73333334922790527
  },
  "Transparency" : 0.044739451142131979,
  "Ansi 1 Color" : {
    "Green Component" : 0,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0
  },
  "Custom Directory" : "No",
  "Horizontal Spacing" : 1,
  "Ansi 4 Color" : {
    "Green Component" : 0,
    "Red Component" : 0,
    "Blue Component" : 0.73333334922790527
  },
  "Ansi 5 Color" : {
    "Green Component" : 0,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0.73333334922790527
  },
  "Use Non-ASCII Font" : false,
  "Ansi 7 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0.73333334922790527
  },
  "Ansi 8 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 0.3333333432674408
  },
  "Ansi 9 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 1,
    "Blue Component" : 0.3333333432674408
  },
  "Ansi 0 Color" : {
    "Green Component" : 0,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Guid" : "B22894EB-E43E-4531-93AA-EE0360C07148"
},
{
  "Ansi 7 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0.73333334922790527
  },
  "Tags" : [

  ],
  "Ansi 12 Color" : {
    "Red Component" : 0.13017468620091677,
    "Color Space" : "sRGB",
    "Blue Component" : 0.90362548828125,
    "Alpha Component" : 1,
    "Green Component" : 0.17663782469840464
  },
  "Ansi 8 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 0.3333333432674408
  },
  "Ansi 9 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 1,
    "Blue Component" : 0.3333333432674408
  },
  "Bold Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Ansi 0 Color" : {
    "Green Component" : 0,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Guid" : "E7A02AE2-BFF5-4120-AB6F-15128AB7EBF7",
  "Rows" : 25,
  "Default Bookmark" : "No",
  "Non-ASCII Anti Aliased" : true,
  "Use Bright Bold" : true,
  "Ansi 10 Color" : {
    "Green Component" : 1,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 0.3333333432674408
  },
  "Ambiguous Double Width" : false,
  "Jobs to Ignore" : [
    "rlogin",
    "ssh",
    "slogin",
    "telnet"
  ],
  "Ansi 15 Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Foreground Color" : {
    "Red Component" : 1,
    "Color Space" : "sRGB",
    "Blue Component" : 1,
    "Alpha Component" : 1,
    "Green Component" : 1
  },
  "Working Directory" : "\/Users\/ayaliz01",
  "Bound Hosts" : [

  ],
  "Blinking Cursor" : true,
  "Disable Window Resizing" : true,
  "Sync Title" : false,
  "Prompt Before Closing 2" : false,
  "BM Growl" : true,
  "Command" : "",
  "Description" : "Default",
  "Mouse Reporting" : true,
  "Screen" : -1,
  "Selection Color" : {
    "Green Component" : 0.8353000283241272,
    "Red Component" : 0.70980000495910645,
    "Blue Component" : 1
  },
  "Columns" : 130,
  "Idle Code" : 0,
  "Ansi 13 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Custom Command" : "No",
  "ASCII Anti Aliased" : true,
  "Non Ascii Font" : "Monaco 12",
  "Vertical Spacing" : 1,
  "Use Bold Font" : true,
  "Option Key Sends" : 0,
  "Selected Text Color" : {
    "Green Component" : 0,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Background Color" : {
    "Red Component" : 0.635284423828125,
    "Color Space" : "sRGB",
    "Blue Component" : 0.25727002881467342,
    "Alpha Component" : 1,
    "Green Component" : 0.25727002881467342
  },
  "Character Encoding" : 4,
  "Ansi 11 Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 0.3333333432674408
  },
  "Use Italic Font" : true,
  "Unlimited Scrollback" : false,
  "Keyboard Map" : {
    "0xf700-0x260000" : {
      "Text" : "[1;6A",
      "Action" : 10
    },
    "0x37-0x40000" : {
      "Text" : "0x1f",
      "Action" : 11
    },
    "0x32-0x40000" : {
      "Text" : "0x00",
      "Action" : 11
    },
    "0xf709-0x20000" : {
      "Text" : "[17;2~",
      "Action" : 10
    },
    "0xf70c-0x20000" : {
      "Text" : "[20;2~",
      "Action" : 10
    },
    "0xf729-0x20000" : {
      "Text" : "[1;2H",
      "Action" : 10
    },
    "0xf72b-0x40000" : {
      "Text" : "[1;5F",
      "Action" : 10
    },
    "0xf705-0x20000" : {
      "Text" : "[1;2Q",
      "Action" : 10
    },
    "0xf703-0x260000" : {
      "Text" : "[1;6C",
      "Action" : 10
    },
    "0xf700-0x220000" : {
      "Text" : "[1;2A",
      "Action" : 10
    },
    "0xf701-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x42",
      "Action" : 11
    },
    "0x38-0x40000" : {
      "Text" : "0x7f",
      "Action" : 11
    },
    "0x33-0x40000" : {
      "Text" : "0x1b",
      "Action" : 11
    },
    "0xf703-0x220000" : {
      "Text" : "[1;2C",
      "Action" : 10
    },
    "0xf701-0x240000" : {
      "Text" : "[1;5B",
      "Action" : 10
    },
    "0xf70d-0x20000" : {
      "Text" : "[21;2~",
      "Action" : 10
    },
    "0xf702-0x260000" : {
      "Text" : "[1;6D",
      "Action" : 10
    },
    "0xf729-0x40000" : {
      "Text" : "[1;5H",
      "Action" : 10
    },
    "0xf706-0x20000" : {
      "Text" : "[1;2R",
      "Action" : 10
    },
    "0x34-0x40000" : {
      "Text" : "0x1c",
      "Action" : 11
    },
    "0xf700-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x41",
      "Action" : 11
    },
    "0x2d-0x40000" : {
      "Text" : "0x1f",
      "Action" : 11
    },
    "0xf70e-0x20000" : {
      "Text" : "[23;2~",
      "Action" : 10
    },
    "0xf702-0x220000" : {
      "Text" : "[1;2D",
      "Action" : 10
    },
    "0xf703-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x43",
      "Action" : 11
    },
    "0xf700-0x240000" : {
      "Text" : "[1;5A",
      "Action" : 10
    },
    "0xf707-0x20000" : {
      "Text" : "[1;2S",
      "Action" : 10
    },
    "0xf70a-0x20000" : {
      "Text" : "[18;2~",
      "Action" : 10
    },
    "0x35-0x40000" : {
      "Text" : "0x1d",
      "Action" : 11
    },
    "0xf70f-0x20000" : {
      "Text" : "[24;2~",
      "Action" : 10
    },
    "0xf703-0x240000" : {
      "Text" : "[1;5C",
      "Action" : 10
    },
    "0xf701-0x260000" : {
      "Text" : "[1;6B",
      "Action" : 10
    },
    "0xf702-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x44",
      "Action" : 11
    },
    "0xf72b-0x20000" : {
      "Text" : "[1;2F",
      "Action" : 10
    },
    "0x36-0x40000" : {
      "Text" : "0x1e",
      "Action" : 11
    },
    "0xf708-0x20000" : {
      "Text" : "[15;2~",
      "Action" : 10
    },
    "0xf701-0x220000" : {
      "Text" : "[1;2B",
      "Action" : 10
    },
    "0xf70b-0x20000" : {
      "Text" : "[19;2~",
      "Action" : 10
    },
    "0xf702-0x240000" : {
      "Text" : "[1;5D",
      "Action" : 10
    },
    "0xf704-0x20000" : {
      "Text" : "[1;2P",
      "Action" : 10
    }
  },
  "Window Type" : 0,
  "Cursor Type" : 1,
  "Background Image Location" : "",
  "Blur" : false,
  "Scrollback Lines" : 1000,
  "Send Code When Idle" : false,
  "Close Sessions On End" : true,
  "Terminal Type" : "xterm-256color",
  "Visual Bell" : true,
  "Flashing Bell" : false,
  "Silence Bell" : false,
  "Ansi 14 Color" : {
    "Green Component" : 1,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 1
  },
  "Name" : "Mongo (Hori)",
  "Cursor Text Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Shortcut" : "",
  "Cursor Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0.73333334922790527
  },
  "Transparency" : 0,
  "Ansi 1 Color" : {
    "Green Component" : 0,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0
  },
  "Ansi 2 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Ansi 3 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0
  },
  "Custom Directory" : "No",
  "Right Option Key Sends" : 0,
  "Ansi 6 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0,
    "Blue Component" : 0.73333334922790527
  },
  "Horizontal Spacing" : 1,
  "Normal Font" : "Monaco 12",
  "Ansi 4 Color" : {
    "Green Component" : 0,
    "Red Component" : 0,
    "Blue Component" : 0.73333334922790527
  },
  "Ansi 5 Color" : {
    "Green Component" : 0,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0.73333334922790527
  },
  "Use Non-ASCII Font" : false
},
{
  "Ansi 7 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0.73333334922790527
  },
  "Tags" : [

  ],
  "Ansi 12 Color" : {
    "Red Component" : 0.15824025264009833,
    "Color Space" : "sRGB",
    "Blue Component" : 0.773162841796875,
    "Alpha Component" : 1,
    "Green Component" : 0.1951802078231008
  },
  "Ansi 8 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 0.3333333432674408
  },
  "Ansi 9 Color" : {
    "Green Component" : 0.3333333432674408,
    "Red Component" : 1,
    "Blue Component" : 0.3333333432674408
  },
  "Bold Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Ansi 0 Color" : {
    "Green Component" : 0,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Guid" : "D0EDE65F-8085-4B55-95A4-173BA4359CCD",
  "Link Color" : {
    "Red Component" : 0.25493556447327137,
    "Color Space" : "sRGB",
    "Blue Component" : 0.57489013671875,
    "Alpha Component" : 1,
    "Green Component" : 0.41144609621475381
  },
  "Rows" : 25,
  "Default Bookmark" : "No",
  "Non-ASCII Anti Aliased" : true,
  "Use Bright Bold" : true,
  "Ansi 10 Color" : {
    "Green Component" : 1,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 0.3333333432674408
  },
  "Ambiguous Double Width" : false,
  "Jobs to Ignore" : [
    "rlogin",
    "ssh",
    "slogin",
    "telnet"
  ],
  "Ansi 15 Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Foreground Color" : {
    "Red Component" : 1,
    "Color Space" : "sRGB",
    "Blue Component" : 1,
    "Alpha Component" : 1,
    "Green Component" : 1
  },
  "Working Directory" : "\/Users\/ayaliz01",
  "Bound Hosts" : [

  ],
  "Blinking Cursor" : true,
  "Disable Window Resizing" : true,
  "Sync Title" : false,
  "Prompt Before Closing 2" : false,
  "BM Growl" : true,
  "Command" : "",
  "Description" : "Default",
  "Mouse Reporting" : true,
  "Screen" : -1,
  "Selection Color" : {
    "Green Component" : 0.8353000283241272,
    "Red Component" : 0.70980000495910645,
    "Blue Component" : 1
  },
  "Columns" : 130,
  "Idle Code" : 0,
  "Ansi 13 Color" : {
    "Red Component" : 0.92803955078125,
    "Color Space" : "sRGB",
    "Blue Component" : 0.92803955078125,
    "Alpha Component" : 1,
    "Green Component" : 0.41600063908845186
  },
  "Custom Command" : "No",
  "ASCII Anti Aliased" : true,
  "Non Ascii Font" : "Monaco 12",
  "Vertical Spacing" : 1,
  "Use Bold Font" : true,
  "Option Key Sends" : 0,
  "Selected Text Color" : {
    "Green Component" : 0,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Background Color" : {
    "Red Component" : 0.25098039215686274,
    "Color Space" : "sRGB",
    "Blue Component" : 0.25098039215686274,
    "Alpha Component" : 1,
    "Green Component" : 0.47450980392156861
  },
  "Character Encoding" : 4,
  "Ansi 11 Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 0.3333333432674408
  },
  "Use Italic Font" : true,
  "Unlimited Scrollback" : false,
  "Keyboard Map" : {
    "0xf700-0x260000" : {
      "Text" : "[1;6A",
      "Action" : 10
    },
    "0x37-0x40000" : {
      "Text" : "0x1f",
      "Action" : 11
    },
    "0x32-0x40000" : {
      "Text" : "0x00",
      "Action" : 11
    },
    "0xf709-0x20000" : {
      "Text" : "[17;2~",
      "Action" : 10
    },
    "0xf70c-0x20000" : {
      "Text" : "[20;2~",
      "Action" : 10
    },
    "0xf729-0x20000" : {
      "Text" : "[1;2H",
      "Action" : 10
    },
    "0xf72b-0x40000" : {
      "Text" : "[1;5F",
      "Action" : 10
    },
    "0xf705-0x20000" : {
      "Text" : "[1;2Q",
      "Action" : 10
    },
    "0xf703-0x260000" : {
      "Text" : "[1;6C",
      "Action" : 10
    },
    "0xf700-0x220000" : {
      "Text" : "[1;2A",
      "Action" : 10
    },
    "0xf701-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x42",
      "Action" : 11
    },
    "0x38-0x40000" : {
      "Text" : "0x7f",
      "Action" : 11
    },
    "0x33-0x40000" : {
      "Text" : "0x1b",
      "Action" : 11
    },
    "0xf703-0x220000" : {
      "Text" : "[1;2C",
      "Action" : 10
    },
    "0xf701-0x240000" : {
      "Text" : "[1;5B",
      "Action" : 10
    },
    "0xf70d-0x20000" : {
      "Text" : "[21;2~",
      "Action" : 10
    },
    "0xf702-0x260000" : {
      "Text" : "[1;6D",
      "Action" : 10
    },
    "0xf729-0x40000" : {
      "Text" : "[1;5H",
      "Action" : 10
    },
    "0xf706-0x20000" : {
      "Text" : "[1;2R",
      "Action" : 10
    },
    "0x34-0x40000" : {
      "Text" : "0x1c",
      "Action" : 11
    },
    "0xf700-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x41",
      "Action" : 11
    },
    "0x2d-0x40000" : {
      "Text" : "0x1f",
      "Action" : 11
    },
    "0xf70e-0x20000" : {
      "Text" : "[23;2~",
      "Action" : 10
    },
    "0xf702-0x220000" : {
      "Text" : "[1;2D",
      "Action" : 10
    },
    "0xf703-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x43",
      "Action" : 11
    },
    "0xf700-0x240000" : {
      "Text" : "[1;5A",
      "Action" : 10
    },
    "0xf707-0x20000" : {
      "Text" : "[1;2S",
      "Action" : 10
    },
    "0xf70a-0x20000" : {
      "Text" : "[18;2~",
      "Action" : 10
    },
    "0x35-0x40000" : {
      "Text" : "0x1d",
      "Action" : 11
    },
    "0xf70f-0x20000" : {
      "Text" : "[24;2~",
      "Action" : 10
    },
    "0xf703-0x240000" : {
      "Text" : "[1;5C",
      "Action" : 10
    },
    "0xf701-0x260000" : {
      "Text" : "[1;6B",
      "Action" : 10
    },
    "0xf702-0x280000" : {
      "Text" : "0x1b 0x1b 0x5b 0x44",
      "Action" : 11
    },
    "0xf72b-0x20000" : {
      "Text" : "[1;2F",
      "Action" : 10
    },
    "0x36-0x40000" : {
      "Text" : "0x1e",
      "Action" : 11
    },
    "0xf708-0x20000" : {
      "Text" : "[15;2~",
      "Action" : 10
    },
    "0xf701-0x220000" : {
      "Text" : "[1;2B",
      "Action" : 10
    },
    "0xf70b-0x20000" : {
      "Text" : "[19;2~",
      "Action" : 10
    },
    "0xf702-0x240000" : {
      "Text" : "[1;5D",
      "Action" : 10
    },
    "0xf704-0x20000" : {
      "Text" : "[1;2P",
      "Action" : 10
    }
  },
  "Window Type" : 0,
  "Cursor Type" : 1,
  "Background Image Location" : "",
  "Blur" : false,
  "Scrollback Lines" : 1000,
  "Send Code When Idle" : false,
  "Close Sessions On End" : true,
  "Terminal Type" : "xterm-256color",
  "Visual Bell" : true,
  "Flashing Bell" : false,
  "Silence Bell" : false,
  "Ansi 14 Color" : {
    "Green Component" : 1,
    "Red Component" : 0.3333333432674408,
    "Blue Component" : 1
  },
  "Name" : "SSH (Vert)",
  "Cursor Text Color" : {
    "Green Component" : 1,
    "Red Component" : 1,
    "Blue Component" : 1
  },
  "Shortcut" : "",
  "Cursor Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0.73333334922790527
  },
  "Transparency" : 0,
  "Ansi 1 Color" : {
    "Green Component" : 0,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0
  },
  "Ansi 2 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0,
    "Blue Component" : 0
  },
  "Ansi 3 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0.73333334922790527,
    "Blue Component" : 0
  },
  "Custom Directory" : "No",
  "Right Option Key Sends" : 0,
  "Ansi 6 Color" : {
    "Green Component" : 0.73333334922790527,
    "Red Component" : 0,
    "Blue Component" : 0.73333334922790527
  },
  "Horizontal Spacing" : 1,
  "Normal Font" : "Monaco 12",
  "Ansi 4 Color" : {
    "Red Component" : 0.027833297848701477,
    "Color Space" : "sRGB",
    "Blue Component" : 0.8212890625,
    "Alpha Component" : 1,
    "Green Component" : 0.16880259977859974
  },
  "Ansi 5 Color" : {
    "Red Component" : 0.8687744140625,
    "Color Space" : "sRGB",
    "Blue Component" : 0.86308636763911362,
    "Alpha Component" : 1,
    "Green Component" : 0.47443492896854877
  },
  "Use Non-ASCII Font" : false
}
]
}
