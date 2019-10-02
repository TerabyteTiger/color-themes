# color-themes

This is a project to walk through the process of creating a Pull Request by contributing to a small open source site! 

## Learn about git - If you're new to git / GitHub, start here 👇
https://dev.to/tvanblargan/crash-course-git-lingo-1enj

## Tutorial for submitting a theme - If you're new to submitting PR's, start here 👇
https://dev.to/12vanblart/make-your-first-pull-request-3iai

## How to
The themes are listed in the `src/assets/themes.json` file. Please add your new theme to the end of the list of themes!

__Properties of a Theme:__

| Key | Description |
|:-----|:-----|
| name | this is where you'll add the css class to be applied when selected |
| title | The name to display on the Theme Picker Element |
| contributor | github username of contributor (If left blank, default github image will be used instead) |

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```
