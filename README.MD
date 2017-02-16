# Discord Server Landing Page
*(Red-DiscordBot-inspired)*

>There are never enough landing pages, huh?

## Support and get design sources!
I'm creating these pages absolutely free of charge, and if you like them - [consider supporting me on Patreon!](https://patreon.com/orels1) You will also get a role on my discord server, as well as access to all the designs (and their sources) that I make.

## Usage

### The simplest way
We'll be fancy and use Codepen.io!

First, you'll need to [open the pen](http://codepen.io/orels/pen/bgZXNP) and edit everything you need.

You might want to edit text inside the `section` tags, as well as `footer`

##### To change the images - simply change the urls to them in the `css` section of the editor, on top

`$background` is the main website background  
`$intro` is the website's blueish section background  
`$image1` is the first image  
`$image2` is the second image

##### To add more sections you'll need to do the following:

* Add it to the menu, by adding this code to the `nav.topmenu`

```pug
a(href="#your_section_name") Your Section
.line.align-self-center
```

* Duplicate `section` tag with all it's contents
* Change section's ID by typing `#your_section_name` instead of what's in there currently
* Change image class to `image3`
* Add new image url to css tab of the editor like this

```sass
$image3: url('../img/image3.jpg')
```

* Add new image class to css tab of the editor after the `image2` like this

```sass
&.image3
  background-image: $image3
```

**Make sure your `&.image3` is on the same indentation level as `&.image2`**


##### To download final results
* Click on the `Export` button on the bottom-right and select `Export .zip`
* Don't forget to create the `img` folder and put all your images in it
* Upload the `index.html` along with `css` and `img` folders to your server. Everything else is not needed

### Simple way
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

### Smart way

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