# Content
This is a repository to control and deploy my personal website sebastian-knigge.eu.

# HTML
My homepages content is custom HTML code in the following directory: [sebastian-knigge.eu](./sebastian-knigge.eu/) 

``` 
.  
├── .github................ Github actions to deploy code  
└── sebastian-knigge.eu.... HTML code  
    ├── img................ Images  
    └── subpages........... All pages except index.html  
        └── Articles....... Directory containing article subpages  
            └── Figures.... Figures used in articles (jpg, png, pdf)
```

# Deploy
A GitHub action is set on the main branch. I.e., whenever there is a PR or push to the main (remote) branch the [sebastian-knigge.eu](./sebastian-knigge.eu/) is pushed to the s3 bucket hosting a static webpage and automatically made public. The CloudFront distribution is invalidated to update the cash. The action is defined in [.github/workflows/main.yaml](./.github/workflows/main.yaml).

