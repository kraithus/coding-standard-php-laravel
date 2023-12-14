# 1. Software Versioning Tool
`Github Desktop` is what will be used. I am a strong advocate of using the terminal but for Github, I am a proud normie. You SHOULD not use the terminal unless you fully understand every jargon of `git` command out there.

# 2. Repositories
>It was peace and quiet before `git init`

## 2.1. Repository Naming
Repository names must be short and concise, in lowercase, no spaces but rather hyphens.
*Examples*:
- project-list
- who-is-that-idol
- algorithmic-recipe-ideas

## 2.2. Repository Requirements
Must contain a `README` file with the `.md` extension. This may be blank but it must exist before the first push. Sample Contents of the `README.md`:
- Project Title followed by a brief description
- Installation and Setup(If Applicable)
- Usage and Features
- Contributing and Support, if applicable provide guidelines for reporting issues and requesting collaboration
- Documentation and Demo: Provide links to the comprehensive documentation and the demo

# 3. Branches
For any project, at start there shall be 2 branches; `development` and `master`. `development` shall be used for the initial basic setup: database(migrations, factories, seeders), auth(breeze/jetstream)

Going forward from there, for each feature/task a new branch must be created. 

## 3.1. Naming of feature branches
`feature/feature-name`. Literal example: `feature/user-authentication`. Do remind me for us to have a demonstration of this.

# 4. Git Etiquette
Yeah I just coined that, maybe it already exists.

## 4.1. Pulling, committing, pushing, merge requests
Always pull before you push anything. Even if you're working alone, just so it sticks with you.

Always include a `commit` description and not just a summary.

Commits should represent single logical changes, makes it easier to rollback if needed, do not want to see what I used to do:
`added feature x, added feature y, bug fix of feature z, deleted go-home.blade.php`

Remember, all changes MUST be pushed to either `feature/branch-name` or `development` never to the `master` branch.

Even after your merge request has been approved or you approve one, you MUST never delete that feature branch
