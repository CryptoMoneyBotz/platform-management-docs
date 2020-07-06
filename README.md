# Axway-Open-Docs

Axway-Open-Docs is a docs-as-code implementation for Axway documentation. It is built using [Hugo](https://gohugo.io/) static site generator with the [Google Docsy](https://github.com/google/docsy) theme. The site is deployed on Netlify at <https://axway-open-docs.netlify.com/>

This repository contains all files for building and deploying the site. The Markdown files for the documentation are stored at `/content/en/docs`.

## Contribute

We welcome your contributions! To get started, go to <https://axway-open-docs.netlify.com/> and click **Documentation** in the top menu. Browse the documentation and use the options in the right navigation to edit any page using GitHub or Netlify CMS.

Before you start contributing, please read the [contribution guidelines](https://axway-open-docs.netlify.com/docs/contribution_guidelines/).

## Create your own microsite using this repository

This section details how to create your own microsite in the Axway-Open-Docs ecosystem. For an overall view of the microsite architecture, see XXX.

### Before you start

You must have completed all of the steps in [Set up and work locally](https://axway-open-docs.netlify.app/docs/contribution_guidelines/setup_work_locally/).

**TBD: What prereqs still apply with new build scripts? Just install Hugo and NodeJS?**

### Create a new microsite repository in Axway org

1. Go to [Axway org on GitHub](https://github.com/Axway) and click **New**.
2. At the top of the page click **Import a repository**.
3. On the next screen, enter the clone URL of this repository and the name for your new microsite.

    * To find the clone URL of this repository, click the drop-down arrow on the Code button above and copy the URL to your clipboard.
    * Enter a name following the naming convention `MYPROJECT-open-docs`, for example `amplify-central-open-docs`.

### Clone the new microsite repository to your local environment

Clone your new repository:

```
cd ~
git clone --recurse-submodules --depth 1 git@github.com:Axway/MYPROJECT-open-docs.git
```

**TBD: Is recurse option needed with new build scripts?**

You must use `--recurse-submodules` or you will not pull down the Docsy theme code you need to generate a working site.

After running these commands, you will have a local copy of the repository in the following location:

```
/home/YOUR-UNIX-USERNAME/MYPROJECT-open-docs
```

### Build the site locally

**TBD: Does user need to install postcss etc with new build scripts?**

Run the hugo server command in your site root:

```
cd ~/open-docs-MYPROJECT/
hugo server
```

The website is now available locally at `http://localhost:1313/`.

### Create a new Netlify microsite

Create a new site from your microsite repo in Netlify and add the axway-open-docs GitHub Oauth provider client and secret to the microsite settings in Netlify (under **Access control > Oauth**).

### Customize the site to use your Github repo

Change the `github_repo` parameter in config.toml to point to your project repo as this is used by Hugo/Docsy to generate the GitHub edit links on each page. For example:

```
github_repo = "https://github.com/Axway/MYPROJECT-open-docs"
```

### Customize the site to use your Netlify CMS instance

Make the necessary changes to get the **Edit on Netlify CMS** links to work correctly.

**TBC but might include**:

* Change base URL in `config.toml` to the URL of your microsite?
* Change `repo` and `site url` in `config.js` to point to your repo/microsite?
* Update the collections in `config.js` to match your docs

### Customize the content for your project

The project contains placeholder documentation content in the folder `/content/en/docs` and placeholder images in `/static/Images`. The placeholder content is copied from the [Docsy example project](https://example.docsy.dev/) (with some modifications) and shows the different types of content and the different types of formatting that are available for you to use when creating your own content.

You must replace or update the placeholder content as necessary with your own documentation content.

When working with the content it can be useful to read the following Docsy documentation to get an understanding of how to add content files and images, and how to change the navigation of the content using frontmatter fields in Markdown files:

* [Adding Content](https://www.docsy.dev/docs/adding-content/content/)
* [Navigation and Search](https://www.docsy.dev/docs/adding-content/navigation/)

### Customize the microsite landing page

The landing page for the microsite is a HTML page `content/en/_index.html` and uses Docsy content blocks. You must modify this page to create your own blocks and link to your own content.

### Connect your microsite to the Axway-Open-Docs ecosystem

When you and your stakeholders are happy with the content on your Netlify microsite, you can request that your microsite be added to the overall ecosystem. This involves having redirects added to the main [Axway Open Documentation](https://axway-open-docs.netlify.app/) site to redirect all traffic to your documentation to your microsite. Contact @alexearnshaw or @andreamussap to request this.

### Set up publishing to Zoomin

To enable publishing of the microsite content as a new _bundle_ on Zoomin production doc portal you must create a classification file, properties file, and zip file as detailed in [Docs-as-code on Zoomin](https://techweb.axway.com/confluence/display/RDAPI/Docs-as-code+on+Zoomin).

When this is set up you must manually FTP the zip file to Zoomin to trigger an upload of the Netlify microsite content.