# OSX Plist
## Managing Plists


### Start and Stop

**start**
`sudo launchctl load -w /Library/LaunchDaemons/com.jingo.start.plist`

**stop**
`sudo launchctl unload -w /Library/LaunchDaemons/com.jingo.start.plist`


### Debug OSX plist launch

The standard out and error keys are very useful, I redirected mine to the first terminal/shell as follows:

```
<key>StandardOutPath</key>
<string>/dev/ttys000</string>
<key>StandardErrorPath</key>
<string>/dev/ttys000</string>
```

You can change ttys000 to another number (ttys001..2) if you have multiple terminals. You can find the terminal id by typing in the shell:

`tty`