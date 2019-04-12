# Asebi 🌺

[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

**Easy image optimization for your custom build process.**  
The goal of this project is to create a simple to use, opinionated API around image-min to optimize
your image files, that can be called as a node script in your build process. See below for an example.

#### Features

- Image optimization with imagemin
- Create webp versions of images
- Resize images with sharp

### Usage

```bash
npm install --dev asebi
```

Then, import and use the library:

```javascript
const { asebi } = require('asebi');

const config = {
  webp: true,
}

(async () => {
  await asebi.resize('src/assets/images', 'dist/images', { sizes: [210, 420], pattern: '[name]_[size].[extension]' });
  await asebi.images('dist/images', 'public/images', config);
})();
```

![](https://i.imgur.com/g85Wlf0.png)
