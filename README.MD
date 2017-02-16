# Discord Server Landing Page
*(Red-DiscordBot-inspired)*

>There are never enough landing pages, huh?

## Support and get design sources!
I'm creating this pages absolutely free of charge, and if you like them - [consider supporting me on Patreon!](https://patreon.com/orels1) You will also get a role on my discord server, as well as access to all the designs (and their sources) that I make.

## Usage
#### Simple way
Download the .ZIP archive, extract everything, get the files inside `__build` folder, edit and upload them to your host.

All the images should be modified inside `styles.css`

`body` - main website background  
`.header` - website blueish intro section background  
`.image1` - first image  
`.image2` - second image

*P.S. You can add more sections to the page, just duplicate one of the existion `<section>` tags, change its contents and give the image `image3` class  
Then put your image into the `img` folder and in the `styles.css` add this*

```css
section .image.image3 {
    background-image: url("../img/<your_image_name>"); }
```

#### Smart way

* [Get Node (LTS)](https://nodejs.org)
* [Get Sass (and Ruby)](http://sass-lang.com/install)

Run
```bash
npm install --only=dev
```
and
```bash
bower install
```

Edit source files inside `src` folder. I'm using `Pug` for templates and `Sass` for styles. Don't know what those are? Google them! They're pretty neat ;)

`index.pug` contains all the html  
`styles.sass` has all the styles

I extracted links to the images into variables on top of the `.sass` files, so you can easily change them in one place

`$background` is the main website background
`$intro` is the website's blueish section background
`$image1` is the first image
`$image2` is the second image

After editing run (inside `src` folder)

```bash
pug views/index.pug --out ../__build
```
and
```bash
sass --no-cache --update css/styles.sass:../__build/css/styles.css 
```

Now you can upload all the files from __build to your server

**Don't forget to put all the images into `img` folder inside `__build` before upload!**

#### Why so much effort?

If you learn it once - you will be able to write html and css much-much faster. For example - to convert this page from a .Sketch design into the actual code - took me less than 2 hours from complete scratch and bootstrap

## Licenses and yada-yada

**Built with Bootstrap v4**

*All the images are property of Supergiant Games, creators of Transistor*

Distributed under MIT