<h1 align="center">Discord Theme Template</h1>
This is basic outline of how I structure a theme. Don't use this as bible documentation. As I speak instructively, I'm more so justifying why I arrange things this specific way. Please feel free to use this template! 

## ThemeName.theme.css

In the way we are setting things up, think of this as the heart of your theme. This is the file where you put your CSS edits. 

BetterDiscord recognizes a theme with the `.theme.css` extension. Powercord and Vizality *do not* require your css file to have this extension. This is a personal choice I use to insure compatibility across all client mods.

Powercord and Vizality are more flexible for themes, because themes for those client mods exist in folders, allowing you to import assets and even other CSS files locally.

BetterDiscord themes are stored as one file. In order for BetterDiscord to recognize your theme, the top of your `.theme.css` file should have something along the lines of:

```css
/**
 * @name ThemeName
 * @author Author
 * @version 0.1a
 * @description An awesome Discord theme!
 * @source https://github.com/Author/ThemeNameRepo
 * @website https://optional.github.io/
*/
```
# ![img](https://files.catbox.moe/ob562k.png)

After this line should be the rest of your CSS file.

Personally, I use this file to import from another CSS file hosted on https://slippinggitty.github.io so that the theme can update without one having to `git pull` for theme updates. Of course, if you are going to be constantly updating local assets, this is might not be a method you would want to use. 

You can import a CSS file by using the `@import url(" ");` tag. Here's an example:

```
@import url("https://author.github.io/ThemeName.css");
```

##  powercord_manifest.json

This is how Powercord recognizes your theme. 

```
{
    "name": "ThemeName",
    "version": "0.1a",
    "license": "MIT",
    "theme": "ThemeName.theme.css",
    "author": "Author",
    "description": "An awesome Powercord theme!"
}
```

# ![img](https://files.catbox.moe/3lwe0v.png)

This file should be self explainitory. Powercord will give details about your theme by specifying them in this structure in the `powercord_manifest.json` file. Powercord can even give details about your theme's license if it recognizes it (data is pulled from choosealicense.com).  

# ![img](https://files.catbox.moe/weh0uh.png)

By adding an "a" to the end of your theme's version number, a little flask icon will indicate that your theme is in alpha. (An example is shown in the image above)

## manifest.json

```
{
    "icon": "assets/icon.png",
    "name": "ThemeName",
    "description": "An awesome Vizality theme!",
    "version": "0.1a",
    "author": "Author",
    "theme": "ThemeName.theme.css",
    "license": "MIT"
}
```
**SIDE NOTE:** Vizality is still in alpha. As such, I cannot include pictures of what the mod's theme manager looks like. 

This file is *just* like the Powercord one, but is intended for Vizality. You can also include an icon for your theme by specifying one. As an example, `"assets/icon.png"` would point to an image named `icon.png` in a folder titled `assets` in the theme's folder.

# ![img](https://files.catbox.moe/i0zqtb.png)

