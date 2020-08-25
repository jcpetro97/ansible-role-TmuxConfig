# TmuxConfig

This role was written to copy the tmux config into place.  ( /home/username/.tmux.conf)
If the username is jxpsys, and the location is Work, then it will copy the .tmux.startup to the home directory as well

#### Variables

| Parameter | Choices | Comments |
| --------- | ------- | -------- |
| `UserName`| | Username where config will be copied to|
| `Location` | Choices:<ul><li>home</li><li>work</li></ul> |Set for customizations I have for work or home.|
| `TmuxStartup` | Choices:<ul><li>yes</li><li>no</li></ul> |Set to yes if you want the .tmux.startup copied into the homedir.  Selecting no will not copy the file|


#### Role Execution

```
roles:
  - {role: TmuxConfig, UserName: "testuser", Location: "home", TmuxStartup: "yes"}

roles:
  - role: TmuxConfig
    vars:
      UserName: "testuser"
      Location: "home"
      TmuxStartup: "yes"

```