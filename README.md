SPARC Community-Owned Infrastructure Microsite
=====

# About

This site provides a custom home for SPARC's Community-Owned Infrastructure project materials.

# How to make a new post via Github web interface

* Clicking [here](https://github.com/sparcopen/infrastructure/new/dev/_posts). That will start a new post in [`_posts`](https://github.com/sparcopen/infrastructure/tree/dev/_posts) on the `dev` branch.
* Give your post a name. Your name must start with the date you want it posted plus a friendly title and `.md` at the end. This means post names look like this YYYY-MM-DD-your-title.md
* Start writing. It can be helpful to [start by copying template](https://github.com/sparcopen/infrastructure/edit/dev/_drafts/template.md).
* When you're ready to save, hit `commit changes` at the bottom.
* In about a minute you'll find your post at http://test.infrastructure.sparcopen.org/. This will only happen if the post date is *today*. Think of this as a preview, it won't show up on Google or anything like that.
* If you want to make edits to your post, find it in [`_posts`](https://github.com/sparcopen/infrastructure/tree/dev/_posts)
* Once you're happy, it's time to put your post on the live site. To go that, [click here](https://github.com/sparcopen/infrastructure/compare/dev?expand=1). If it shows only your post as being added, great! If it doesn't, best to reach out to Joe for help. If that isn't possible, clicking [here](https://github.com/sparcopen/infrastructure/new/live/_posts) and copy your post. This will put your post directly on live, and while this can be bad practice is fine in a pinch.

# How to add different type of content

* Threads: Go to `_topics`, duplicate any file and adjust to your liking.
* Reports: Go to `_reports`, duplicate any file and adjust to your liking.
* Media (e.g images): Go to `_reports`, duplicate any file and adjust to your liking.


# About the code

The live version of the site is at https://infrastructure.sparcopen.org/ (using `live` in this repo). [![Netlify Status](https://api.netlify.com/api/v1/badges/547e2215-6ab1-4a29-84f1-ef0d8fa8b508/deploy-status)](https://app.netlify.com/sites/upbeat-swirles-009f3e/deploys)

A dev version is at https://test.infrastructure.sparcopen.org/ (using `dev` in this repo). An earlier version existing in Joe's personal repo but this has been retired. [![Netlify Status](https://api.netlify.com/api/v1/badges/01cb4f7c-2d26-4eed-ba5b-70084a7ae9a6/deploy-status)](https://app.netlify.com/sites/keen-panini/deploys)

Another version of the site for members exists too.

The site uses Jekyll as a build system, and Netlify for server / CDN.

We forked the original codebase from https://github.com/dbtek/dbyll however we likely stripped just about everything out during the build.
