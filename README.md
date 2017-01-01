#nmssavetool
A command line tool to decrypt, encrypt, and modify No Man's Sky game save files
===============================================

Created by [Matthew Humphrey](https://github.com/matthew-humphrey)

This is a simple tool to allow decoding, encoding, and convenient editing operations
on saves for the No Man's Sky game.

Download [precompiled binary](http://www.mediafire.com/file/ezm6yt46yzelu7y/nmssavetool-1.1.zip)

##Usage

Run "nmssavetool help" for help.

```
> nmssavetool help

nmssavetool 1.1.0.0
Copyright c  2016

  decrypt    Decrypt the latest game save slot and write it to a formatted JSON file.

  encrypt    Encrypt a JSON file and write it to the latest game save slot.

  modify     Modify one or more attributes of a game save.

  help       Display more information on a specific command.

  version    Display version information.
```

###decrypt
```
>nmssavetool.exe help decrypt

nmssavetool 1.1.0.0
Copyright c  2016

  -o, --output       Specifies the file to which the decrypted, formatted game save will be written.

  -g, --game-mode    Required. Use saves for which game mode (normal|surival|creative)

  -v, --verbose      Displays additional information during execution.

  --help             Display this help screen.

  --version          Display version information.
```

###encrypt
```
>nmssavetool.exe help encrypt

nmssavetool 1.1.0.0
Copyright c  2016

  -i, --input        Specifies the JSON input file which will be encrypted and written to the latest
                     game save slot.

  --v1-format        When encrypting, use the old NMS V1 format

  -g, --game-mode    Required. Use saves for which game mode (normal|surival|creative)

  -v, --verbose      Displays additional information during execution.

  --help             Display this help screen.

  --version          Display version information.```
```

###modify
```
>nmssavetool.exe help modify

nmssavetool 1.1.0.0
Copyright c  2016

  -a, --all          Maximize exosuit, multi-tool, ship, and freighter inventory, health, fuel, and
                     energy levels. Repair all damage.

  -e, --energy       Maximize exosuit, multi-tool, and ship energy and fuel (hyperdrive and launcher)
                     levels.

  -i, --inventory    Maximize exosuit, multi-tool, ship, and freighter inventory.

  -r, --repair       Repair damage to exosuit, multi-tool, and ship.

  -t, --apply-to     (Default: exosuit multitool ship freighter) What to apply changes to.

  --v1-format        When encrypting, use the old NMS V1 format

  -g, --game-mode    Required. Use saves for which game mode (normal|surival|creative)

  -v, --verbose      Displays additional information during execution.

  --help             Display this help screen.

  --version          Display version information.
```

##Supported commands

* decrypt - Decrypt the latest save game for the specified game mode (normal/survival/creative) and write it to a file whose location you specify.
* encrypt - Encrypt the file you specify and write it to the latest save game slot for the specified game mode.
* modify - Edit the latest game save slot for the specified game mode to repair damage, maximize energy levels, and/or maximize inventory levels.
* help - Provide help on command-line syntax for any command.
* version - Displays the program's version information.

##Changelog

###2016-12-30 1.0.0.0

* Initial release

###2016-12-30 1.1.0.0

* Added damage repair to Refill Command
* Switched to a new command-line parsing library
* Moved to a verb-style command line interface, and provide more fine-grained control over modifications.
* Minor refactoring to reduce duplicated code
