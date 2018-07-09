# Resume

Created from [hugo Resume](https://github.com/eddiewebb/hugo-resume).

This is basically a single-page website with auto-scrolling based on left-hand nav.

- [Resume](#resume)
	- [Examples](#examples)
	- [Setup & Use](#setup-&-use)
		- [Summary](#summary)
		- [Data files](#data-files)
		- [Projects](#projects)
		- [Publications](#publications)
		- [Template params](#template-params)
	- [Credits](#credits)
		- [hugo Resume](#hugo-resume)

## Examples

See [Carles's site](https://carles2m.com) for a live example.

## Setup & Use

Run the site with the command: `hugo server`

### Summary
Edit the main `content/_index.md` with a brief bio/summary

### Data files
Data files are used for simple content presented on the homepage.

- [data/skills.json](https://github.com/carles2m/resume/blob/master/data/skills.json)
- [data/experience.json](https://github.com/carles2m/resume/blob/master/data/experience.json)
- [data/education.json](https://github.com/carles2m/resume/blob/master/data/education.json)

### Projects
Projects are added to the folders `content/projects/creations` or `content/projects/contributions`. The difference indicates your role as originator or colaborator. Use `hugo add content/projects/TYPE/name-of-project.md` to leverage the proper archetype.

### Publications
Similar to projects, creste them under `content/publications`. Include any papers, speaking engagemnents, articles, etc.

### Template params

All personal information outside the above details is captured by params in [`config.toml`](https://github.com/carles2m/resume/blob/master/config.toml)

```toml
[params]
firstName = "Eddie"
lastName = "Webb"
address = "Rollinsford, NH"
phone = "1-555-555-1234"
contactNote = "Dev Tools Engineer" #used in QR code only
profileImage = "img/me.png"
email = "email@domain.com"
description = "Software Platform Engineer with experience leveraging agile, DevOps, and CI/CD to manage large scale distributed platforms both on prem and in public cloud."
favicon = "images/favicon.ico"

# what sections to display.  Setting to false disables navigation and section.
showSkills = true
showProjects = true
showOpenSource = true
showPublications = true
showExperience = true
showEducation = true

showQr = true

# do you want to show git hash on page footer and link to repo? Add commit URl for repo here.
gitCommitPrefix = "https://github.com/YOURNAME/REPONAME/commit/"


[[params.handles]]
name = "LinkedIn"
link = "https://www.linkedin.com/in/edwardwebb/"

[[params.handles]]
name = "GitHub"
link = "https://github.com/eddiewebb/"

[[params.handles]]
name = "Bitbucket"
link = "https://bitbucket.org/eddiewebb/"

[[params.handles]]
name = "Stack Overflow"
link = "https://stackoverflow.com/users/story/82880"
# optional icon attribute used for Font Awesome icons, otherwise the name is lowercased.
icon = "stack-overflow"

[[params.handles]]
name = "Keybase"
link = "https://keybase.io/edwardawebb"
# optional icon attribute used for Font Awesome icons, otherwise the name is lowercased.
icon = "key"

[params.google.analytics]
trackerID = "XX-123446-01"

[outputs] #only required for search
home = ["HTML", "JSON"]
```

## Credits

This project is based on the hugo Resume theme by Eddie Webb.

### hugo Resume

This is basically a single-page website with auto-scrolling based on left-hand nav. Dedicated project/publications pages allow more detail. Includes a client-side search powered by fuse.js at '/search' but currently theme does not link to that anywhere.

hugo Reume ports the Start Bootstrap Resume theme by David Miller to support hugo.