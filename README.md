# WSNFontStorage

This is how WSN can use fonts from other websites!

This has only been tested on fonts from https://www.fontshare.com/. When downloaded the font from fontshare comes with a helpful "web" folder where I got a CSS file.

## Setting Up ##

1. Download the font and folder from Fontshare.
2. Click "Add a new file" and in the name type in /{name_of_font}/{name-of-font.css}
3. Copy and paste the contents of the Fontshare css file. Path is: Fonts\Fonts\WEB\css
4. Upload the files in the path to the folder you just created: Fonts\Fonts\WEB\fonts
5. Now click into the one of the fonts you want to use.
6. Copy and paste that link into https://raw.githack.com/
7. Get the url on the left "Use URL in production." You should get a URL that looks like this: https://rawcdn.githack.com/ryankawahara/WSNFontStorage/70f821904159967f4ad0322dc6eb45bade82bd81/Clash%20Grotesk/ClashGrotesk-Bold.woff2
8. Copy everything in the URL up until the font name. In this case that would be https://rawcdn.githack.com/ryankawahara/WSNFontStorage/70f821904159967f4ad0322dc6eb45bade82bd81/Clash%20Grotesk/

Now let's go to the CSS file in GitHub.

This is what the CSS file should look like originally.
```
@font-face {
  font-family: 'ClashGrotesk-Variable';
  src: url('../fonts/ClashGrotesk-Variable.woff2') format('woff2'),
       url('../fonts/ClashGrotesk-Variable.woff') format('woff'),
       url('../fonts/ClashGrotesk-Variable.ttf') format('truetype');
       font-weight: 200 700;
       font-display: swap;
       font-style: normal;
}
```

Now copy and paste the new link to replace the ../fonts/ part of the path.

https://rawcdn.githack.com/ryankawahara/WSNFontStorage/70f821904159967f4ad0322dc6eb45bade82bd81/Clash%20Grotesk/

Now it should look like this.
```
@font-face {
  font-family: 'ClashGrotesk-Variable';
  src: url('https://rawcdn.githack.com/ryankawahara/WSNFontStorage/70f821904159967f4ad0322dc6eb45bade82bd81/Clash%20Grotesk/ClashGrotesk-Variable.woff2') format('woff2'),
       url('https://rawcdn.githack.com/ryankawahara/WSNFontStorage/70f821904159967f4ad0322dc6eb45bade82bd81/Clash%20Grotesk/ClashGrotesk-Variable.woff') format('woff'),
       url('https://rawcdn.githack.com/ryankawahara/WSNFontStorage/70f821904159967f4ad0322dc6eb45bade82bd81/Clash%20Grotesk/ClashGrotesk-Variable.ttf') format('truetype');
       font-weight: 200 700;
       font-display: swap;
       font-style: normal;
}
```
Now you can use the following in your CSS in SNO: `font-family: "ClashGrotesk-Variable";`
