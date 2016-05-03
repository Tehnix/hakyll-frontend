# Hakyll Frontend
The Hakyll frontend project strives to provide a CMS like interface to [Hakyll](https://jaspervdj.be/hakyll/) content creation - basically a UI for managing Hakyll.

## Motivation
Currently a Hakyll user has to know how to compile and build a Hakyll site, which doesn't make it very suitable for non-technical users. The frontend will allow non-technical users to edit content on the site and deploy it, without needing to go to the command-line at any point.


# Content Creation
Much like a normal CMS, an admin interface will provide access to creating blog posts and static pages. The format of the files will be markdown, so a typical operation like adding a blog post would go something like this:

1. The user creates a new blog post from the admin interface
    * The frontend creates a file in `hakyll/posts/post-name.md`
2. User fills in content into the post and saves
    * Frontend writes the content to `hakyll/posts/post-name.md`
3. User wants to update the site with the new content, and presses `deploy`
    * Frontend compiles the `hakyll/` folder with __hakyll__
    * Frontend uploads the `_site/` folder (e.g. via rsync) to the deployment location (can be a remote server)

## Additional Functionality
Additional ideas for features:

* Allow CSS to be edited
* Allow JavaScript to be edited
* Managing static content such as images
* User permission management (who can create/edit/delete, who can deploy, etc)
* Allow templates to be edited and created
* Can choose a template on a per post/page basis
* Integration with S3 for static resources (e.g. images)
* Integration with CloudFlare/CloudFront for cache purging


# TODO

- [ ] Create a base Hakyll setup
- [ ] Content
    - [ ] List content files
    - [ ] Editing interface to existing post/page files
    - [ ] Allow new posts/pages to be created
    - [ ] Live preview of markdown content (preferably with site styles applied)
- [ ] Static resources
    - [ ] Editing interface to CSS (can just be one main style file for now)
    - [ ] Editing interface to JavaScript (can be two files, one located in the header and one located at the end of the body)
- [ ] Images
    - [ ] List image files
    - [ ] Upload new image files
    - [ ] Delete existing image files
    - [ ] Allow images to be uploaded to S3
- [ ] Templates
    - [ ] List templates
    - [ ] Editing interface to existing templates
    - [ ] Allow new templates to be created
    - [ ] Allow a content to specify a specific template
- [ ] Deployment
    - [ ] Execute a __hakyll__ build
    - [ ] Upload the `_site/` folder to the deployment location
        - [ ] Allow the deployment location to be local
        - [ ] Allow the deployment location to be remote

