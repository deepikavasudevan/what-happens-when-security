# What can go wrong ...

This is inspired by the [what-happens-when](https://github.com/alex/what-happens-when) that details what happens when you type google.com and press enter.

In this version, we attempt to approach this from a threat modeling/security perspective in as much detail as possible.
[OWASP Threat Modeling Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)

# Table of Contents
## Click the address bar on the browser
https://github.com/BastilleResearch/mousejack
https://www.blackhillsinfosec.com/executing-keyboard-injection-attacks/

## Type http://www.google.com through your keyboard and press Enter
###What Happens When
When you press enter, an electrical circuit specific to the enter key is closed. The state of each key switch is scanned and converted into a keycode. The keycode is encoded and transported to the 
computer either through a Universal Serial Bus (USB) or a Bluetooth connection.  

###What can go wrong  
Keyloggers are software programs or hardware devices that record keystrokes. Anyone with access to the computer can install a keylogger. They could also come as a part of an application installation from an untrusted source. Of course, recording and transmitting keystrokes is innocuous when typing http://www.google.com. But it becomes problematic when typing in login details or financial details.
More information about keyloggers: https://www.veracode.com/security/keylogger

A physical keyboard is easily subject to spoofing over USB or Bluetooth.

Side-channel keyboard attacks
