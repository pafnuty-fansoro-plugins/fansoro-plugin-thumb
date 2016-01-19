# Thumb Plugin for [Fansoro CMS](http://fansoro.org/)

![version](https://img.shields.io/badge/version-1.1.0-brightgreen.svg?style=flat-square "Version")
![Fansoro](https://img.shields.io/badge/Fansoro-2.x-green.svg?style=flat-square "Fansoro Version")
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/pafnuty-fansoro-plugins/fansoro-plugin-thumb/blob/master/LICENSE)

Plugin for creation of thumbnails from images on the page.


## Advantages
- Easy use.
- Automatic generation resized images.
- Gallery mode.
- Five methods of resizing images.


## Install
See [this instruction](http://fansoro.org/documentation/plugins/plugins-installation)

## Usage

### Very simple example
Just wrap the url for the image in `.md` file in shortcode `thumb` and specify the size of the generated thumbs:
```smarty
{thumb size="200"}https://imgholder.ru/600x400.png{/thumb}
```

### A more complex example

```smarty
{thumb 
    size="200x300" 
    method="crop" 
    quality="80" 
    folder="/storage/images/myfolder/" 
    title="My Image Tititle" 
    alt="Alt Image Text"
}
    https://imgholder.ru/600x400.png
{/thumb}
```

### Gallery
```smarty
{thumb 
    size="300" 
    gallery="1" 
    title="Gallery Image 1"
}
    https://imgholder.ru/800x600&text=Gallery+Image+1.png
{/thumb}

{thumb 
    size="300" 
    gallery="1" 
    title="Gallery Image 2"
}
    https://imgholder.ru/820x500&text=Gallery+Image+2.png
{/thumb}

{thumb 
    size="300" 
    gallery="1" 
    title="Gallery Image 3"
}
    https://imgholder.ru/810x650&text=Gallery+Image+3.png
{/thumb}

{thumb 
    size="300" 
    gallery="1" 
    title="Gallery Image 3"
}
    /storage/images/bg.jpg
{/thumb}
```

## Params

| Name | Description | Values | Default |
|------|-------------|--------|---------|
| size | The size of the thumbnails | 200 <br> 300x500 | `false` |
| method | A method of resizing image | exact <br> portrait <br> landscape <br> auto <br> crop | `auto` |
| quality | Image quality | 0-100 | `100` |
| folder | The path from the site root to the folder that will hold the generated thumbnails | `/images/` | `/storage/images/thumb/` |
| title | Link title | Some text | `false` |
| alt | Image alt | Some text | `false` |
| class | Class added to the link | `mynewclass` | `false` |
| gallery | Enable gallery of popup images | `1` | `false` |


## License 
[MIT](https://github.com/pafnuty-fansoro-plugins/fansoro-plugin-thumb/blob/master/LICENSE)