# Website for Kube-platform

To create the static part of the website you have to install [hugo](https://gohugo.io) which is a static website generator written in go. Please see their website on how to install it locally. 

## Creating documentation

To create a new documentation page just use:

```
hugo new --kind docs docs/my-new-doc.md
```

This will create a markdown file under `content/docs/my-new-doc.md`. The subfolder `content` is very important to note here. This is where the source for the website lifes. There is another folder `docs` at the root of this repository, which is the folder where the statically generated content will go to. It has to have that name as it is used by github-pages as the source for the website.

## Working with content

Two see a preview of the content while editing you can start hugo in server-mode using:

```
hugo server -w
```

It will make a generated version of the website available at [http://localhost:1313/](http://localhost:1313/). The flag `-w` will make sure that hugo watches for changes in the source directory so that the become available in the browser immediatly.


## Generating a new version of the website

First you have to generate the static content using:

```
hugo
```

Then create a new git commit and push it to github. This will automatically make the new content available to the public.
