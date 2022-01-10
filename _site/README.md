## How does this repo work?

This repo is built based on [just-the-docs](https://github.com/pmarsceill/just-the-docs) Jekyll theme. The `docs` folder contains all the pages as markdowns. On top of the markdown add this table based on how you want to locate the file.

### To add a file to the main index:

| layout  | title        | nav_order   |
| ------- | ------------ | ----------- |
| default | <title_here> | <nav_order> |

### To add a file to a folder:

Create a folder and place the markdown inside this folder, example: 

| layout  | title                       | parent             | permalink                                        |
| ------- | --------------------------- | ------------------ | ------------------------------------------------ |
| default | Quality Assurance Procedure | Quality Management | /quality-management/quality-assurance-procedure/ |

## Testing Locally

```
cd floodsense.github.io
bundle install
bundle exec jekyll serve --config _config_local.yml
```

 ------------------------------------------------------------------------------------------------------------------------
Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
