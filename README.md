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

 

