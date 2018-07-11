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
firstName = "Carles"
lastName = "Moreno Magrans"
address = "North Bend, WA, US"
profileImage = "img/profile.jpg"
email = "carlesm@outlook.com"
description = "Software Engineer making the web empower everyone to achieve more."

# what sections
showSkills = true
showProjects = true
showOpenSource = false
showPublications = false
showExperience = true
showEducation = true

showQr = false
contactNote = "Software Engineer"

[[params.handles]]
name = "LinkedIn"
link = "https://www.linkedin.com/in/carles2m"

[[params.handles]]
name = "Bitbucket"
link = "https://bitbucket.org/mushn/"

[[params.handles]]
name = "GitHub"
link = "https://github.com/carles2m"

[params.google.analytics]
trackerID = "XX-123446-01"

#only required for search
[outputs]
home = ["HTML", "JSON"]
```

## Credits

This project is based on the hugo Resume theme by Eddie Webb.

### hugo Resume

This is basically a single-page website with auto-scrolling based on left-hand nav. Dedicated project/publications pages allow more detail. Includes a client-side search powered by fuse.js at '/search' but currently theme does not link to that anywhere.

hugo Reume ports the Start Bootstrap Resume theme by David Miller to support hugo.