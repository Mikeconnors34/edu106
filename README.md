# EDU106 IndieWeb Blog Starter

A tiny blog for students in **EDU106: New Literacies**. It is designed for students with no coding experience who will use GitHub, GitHub Pages, and Codex for the first time.

## Why this starter is intentionally small

There is no framework, package manager, database, theme engine, or build process. The whole site is plain HTML and CSS. Students should be able to understand the basic shape of their site even if Codex helps them edit it.

The starter uses Microformats2 so services such as Granary can read the site as structured web content and convert it to feed formats.

## Student setup

1. Fork this repository into your own GitHub account.
2. Open the fork in Codex.
3. Ask Codex: `Help me personalize this EDU106 blog. Change only my name, GitHub username, site description, and first post. Keep all Microformats2 classes intact.`
4. Review the proposed changes before accepting them.
5. In GitHub, open **Settings → Pages**.
6. Under **Build and deployment**, choose **Deploy from a branch**.
7. Select the repository's default branch and `/ (root)`, then save.
8. GitHub will publish your site at a URL similar to `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

## Writing a new post with Codex

Ask Codex:

> Create a new blog post from `posts/hello-world.html`. Give it a short lowercase filename with hyphens. Add the new post to the top of the Latest posts section on `index.html`. Preserve the `h-entry`, `p-name`, `dt-published`, `e-content`, `p-author`, `u-url`, and `u-uid` Microformats2 classes. Do not add a framework or JavaScript.

Then paste your draft or tell Codex what you want to write about.

## Writing a reply post

A reply is a post on **your own site** that responds to something published somewhere else. The important Microformats2 property is `u-in-reply-to`, which points to the original post.

Use `posts/reply-example.html` as the model. Ask Codex:

> Create a reply post from `posts/reply-example.html`. I am replying to: PASTE-URL-HERE. Preserve `h-entry`, `u-in-reply-to`, `dt-published`, `e-content`, `p-author`, `u-url`, and `u-uid`. Add the reply to the top of the home-page feed. Do not add a framework or JavaScript.

Publishing `u-in-reply-to` makes the relationship machine-readable. A full IndieWeb reply workflow can also send a Webmention to the original site, but this static starter does not automatically send Webmentions.

## Microformats used

- `h-card` identifies the author/site owner.
- `h-feed` identifies the stream of posts on the home page.
- `h-entry` identifies each post.
- `p-name` identifies names and post titles.
- `dt-published` identifies a publication date.
- `e-content` identifies the full content of a post.
- `u-url` identifies a URL.
- `u-uid` identifies the canonical/permalink URL.
- `p-author h-card` associates a post with its author.
- `u-in-reply-to` identifies the URL that a reply post responds to.

Do not remove these classes when redesigning the site.

## Granary

Granary can fetch HTML containing Microformats2 and translate it into formats such as Atom, RSS, JSON Feed, and ActivityStreams. After your GitHub Pages site is public, use your public site URL as the source in Granary.

## Course design goal

This project is not a coding class. Students use a small, inspectable website to learn how AI-assisted development works: describing a goal, reviewing generated changes, testing a result, noticing mistakes, revising instructions, and maintaining ownership of a digital space.
