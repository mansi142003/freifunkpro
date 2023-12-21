# Projects

This website was initially created by [coala](https://projects.coala.io) for their GSoC projects. We adopted it.

To view live projects visit [projects.freifunk.net](https://projects.freifunk.net)

## Purpose

This is designed for GSoC but can be used for other initiatives at the same
time. We use it for research theses, GSoC, GCI and maybe others in the future.

Why?

- It's way more appealing to students.
- You can search and filter projects.
- Project ideas as structured data are more concise and you're sure to have all
  points covered - at the same time we can show students an overview and showing
  the full information only when needed.
- A proper review process can be used for triaging and iterating on project
  ideas.
- Stop wasting time maintaining a mentors list. This can be generated from the
  projects.

## Usage

### Dependencies

1. Install [asdf-vm](https://asdf-vm.github.io/asdf/#/core-manage-asdf-vm) for your OS.
2. Using asdf-vm, install [ruby](https://github.com/asdf-vm/asdf-ruby).
3. Install Jekyll

        $ gem install jekyll bundler

### Clone and Run

Clone freifunk Projects repository

    $ git clone https://github.com/freifunk/projects.git

Run freifunk Projects website

    $ cd projects
    $ bundle install
    $ bundle exec jekyll serve

Then you can simply go to either of the following addresses in your browser to access the site:

    127.0.0.1:4000
    localhost:4000

If you face problems while installing Jekyll or using its gem bundler you may go through its [troubleshooting docs](https://jekyllrb.com/docs/troubleshooting/)

## Defining Projects

Mentors and admins can define projects in markdown using the following structure and save it in the ``_projects`` folder with a relevant filename.
A sample project definition is available [here](https://github.com/freifunk/projects/blob/main/_projects/_template.md)

## Defining FAQs

Users can also add FAQs by simply creating a markdown file in _faq folder.

Format for faq markdown file is as follows:
```
---
Question: <Write the question here>
---

Answer
```

## Multi Language Support

freifunk Projects supports multiple 'human languages'. To add a translation of a project
in a language, the following steps can be followed:

- Create a folder with language code in ```data/locale``` folder.
- Create ```faq.json```, ```projects.json```, ```faq``` and ```projects``` folder
if they do not exist already.
- Add translated content of a project inside ```projects``` folder. The names of the
files should be the same.
- Similarly translated content of a faq goes inside ```data/locale/ < language-id > /faq```
folder.
- For the faq.json and projects.json metadata, refer to Bahasa and Hindi
Translations available in ```data/locale``` directory.
- Lastly, in ```resources/js/app.js``` file, Add the new language json in Language service.
