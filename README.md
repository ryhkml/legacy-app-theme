## Fedora GNOME Appearance Legacy Applications
Some applications installed from flatpak might not be able to apply legacy application themes. This shell script i made might help apply the custom themes you set. I've tested this script on a few applications, including Firefox and LibreWolf, and it worked. The theme applied is using gtk-3.0.

> [!WARNING]
> 
> Not all flatpak applications support overriding their theme directories or some flatpak applications might have dedicated options for customizing their appearance

### Get Application ID
To see the installed app IDs, run the command:
```sh
flatpak list --app
```

### Usage
This command gives a flatpak application access to your user's themes, allowing it to potentially use themes you've installed on your system. This can be useful if the application supports themes and you want to use a particular theme from your system. To apply the theme to your application, run the command:
```sh
./apply-theme <APPLICATION ID>
```
> [!NOTE]
> 
> Make sure the theme you want to use is in the directory `~/.themes`