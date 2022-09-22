## Getting Started

This POC builds PR Preview environments as well as hosting the latest and greast build from main using Github actions and pages.

### Github pages setup

1. Create a branch named `gh-pages` from main
1. In Github repo settings, on the Pages Tab. Use `gh-pages` branch and target the `docs` folder.
1. Create a folder in the root of the project named `docs`
1. Create a simple landing page so other devs know the purpose of the folder. Link to `/docs` for the latest and greatest storybook build.
1. Storybook build folder can be anywhere, and should be `.gitignore`d!
1. PR previews will be committed on the `gh-pages` branch and will auto deploy to gh pages - this does take up to 5 mins after the actions complete.
1. The documentation site is built when there is a merge into `main`. It will overwrite the `docs/docs` folder in the `gh-pages` branch with a fresh build from `main`.

### GH Pages URLs:

Documentation Site: [/docs](https://acolpitts-telus.github.io/storybook-preview/docs)

Sample PR Preview URL: `/pr-preview/feat-sample-slug`

## Steps to test

1. First, clone the repo and checkout a new feat branch to test the PR preview build.
1. On a new branch, make a change to the code in the stories folder. This can be a trivial change to the title on `/stories/Introduction.stories.mdx`, it should just be a change that's easy to tell the difference between your PR Preview branch and whats in `main`.
1. Commit and push your changes, and create a pull request on github.
1. After the github action completes, you should see a `Preview environment` comment on the pull request you created.

\*Note: It takes up to five minutes to actually deploy the github pages site once the github action completes, so give it 5 mins before trying/sharing the link.
