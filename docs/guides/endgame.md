# Endgame

<!-- prettier-ignore-start -->
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
## Table of Contents

- [About](#about)
  - [Meet the endgame team](#meet-the-endgame-team)
- [Timeline](#timeline)
  - [Week 1: Project kickoff](#week-1-project-kickoff)
    - [Templates](#templates)
  - [Week 2: Project work](#week-2-project-work)
  - [Week 3: Project work](#week-3-project-work)
  - [Week 4: Pre-endgame planning](#week-4-pre-endgame-planning)
    - [Templates](#templates-1)
  - [Week 5: The endgame](#week-5-the-endgame)
  - [Week 6: Release and planning](#week-6-release-and-planning)
- [Releases](#releases)
  - [Hotfix releases](#hotfix-releases)
    - [Publishing steps](#publishing-steps)
  - [Patch releases](#patch-releases)
    - [Publishing steps](#publishing-steps-1)
  - [Release candidate releases](#release-candidate-releases)
    - [Publishing steps](#publishing-steps-2)
  - [Minor releases](#minor-releases)
    - [Publishing steps](#publishing-steps-3)
  - [Major releases](#major-releases)
    - [Publishing steps](#publishing-steps-4)
- [Testing](#testing)
  - [Procedures](#procedures)
    - [`create-react-app`](#create-react-app)
- [FAQ](#faq)
    - [Making sure your environment is consistent with `upstream`](#making-sure-your-environment-is-consistent-with-upstream)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->
<!-- prettier-ignore-end -->

## About

Inspired by the release process of
[VSCode](https://github.com/Microsoft/vscode/wiki/Development-Process#end-game),
Carbon follows a release process that we refer to as the endgame. Given that our
work is structured in a series of projects across an iteration, the endgame is
an opportunity in the final week of an iteration for us to coordinate final
deliverables, run verification testing, and lean on the Carbon community to help
verify pre-release builds.

### Meet the endgame team

Every release cycle, we have three team members participate in running the
endgame in addition to their project-specific responsibilities. Running the
endgame involves a variety of tasks outlined in our [timeline](#timeline). This
endgame team is composed of a release leader, and two sidekicks. There should be
at minimum one designer and one developer in each endgame team.

The objectives of the release leader include the following:

- Coordinate the initial project proposals into a single iteration cycle
  planning issue that is shared in our issue tracker
- Share through an external blog the top-level objectives of the projects we're
  working for a given cycle
- Help coordinate across projects throughout the project cycle in order to run a
  successful endgame
- Help to familiarize sidekicks with the endgame process so each of them may run
  a future endgame
- Successfully run the endgame at the conclusion of a release cycle

The objectives of the release sidekicks include:

- Assisting the release leader in endgame tasks at the end of the release cycle
- Creating documentation to make the onboarding process easier for future
  sidekicks
- Learning and understanding how to run a future endgame process

After a release cycle completes, the endgame team will be reorganized. The
endgame leader will become a sidekick to help out with the release, and one of
the sidekicks will become the new endgame leader. New team members will fill in
the remaining sidekick role over time.

At a high-level, this sequence might look like the following:

Given the team:

- A (Developer)
- B (Developer)
- C (Designer)
- D (Designer)
- E (Developer)

|            | Leader        | Sidekick 1    | Sidekick 2    |
| ---------- | ------------- | ------------- | ------------- |
| Rotation 1 | A (Developer) | B (Developer) | C (Designer)  |
| Rotation 2 | B (Developer) | C (Designer)  | A (Developer) |
| Rotation 3 | C (Designer)  | D (Developer) | B (Developer) |
| Rotation 4 | D (Developer) | E (Designer)  | C (Designer)  |
| Rotation 5 | E (Designer)  | A (Developer) | D (Developer) |

## Timeline

Release cycles tend to last between four and six weeks. During that time, the
endgame team is responsible for the following high-level milestones:

- [Week 1: Project kickoff](#week-1-project-kickoff)
- [Week 2: Project work](#week-2-project-work)
- [Week 3: Project work](#week-3-project-work)
- [Week 4: Pre-endgame planning](#week-4-pre-endgame-planning)
- [Week 5: The endgame](#week-5-the-endgame)
- [Week 6: Release and planning](#week-6-release-and-planning)

### Week 1: Project kickoff

Checklist:

- [ ] Create monthly planning issue
  - [ ] Reach out to core team to fill our project details (set hard deadline)
- [ ] Write blog post with last release recap + current release plans
  - [ ] Submit post for content review (Connor)
  - [ ] Get blog post banner from design (Jeannie)
  - [ ] Publish and announce via Slack
- [ ] Open website PR to add blog post to homepage and update
      [Roadmap page](https://www.carbondesignsystem.com/updates/roadmap) with
      current release plans
- [ ] Schedule future meetings:
  - [ ] Week 3: Thursday mid-project demo day (1 hr)
  - [ ] Week 6: Tuesday final demo day (1hr)
  - [ ] Week 6: Thursday release retro (1-2 hrs)
  - [ ] Week 6: Thursday project planning meeting (1 hr)

#### Templates

<details>
  <summary>Month planning issue template</summary>

```md
<!-- Issue title: Month Year Planning -->
<!-- Example: August 2019 Planning -->

# Endgame

- **September 2nd, 2019:** Project phases begins
- **September 30th, 2019:** Endgame starts
- **October 2nd, 2019:** Code freeze for endgame
- **October 7th, 2019:** Expected release date

## Projects

### 1. `Project title`

> Project description

#### Squad

- Member
- Member
- Member

#### Primary goals

- TBD

#### Stretch goals

- TBD

#### Deferred goals

- TBD
```

</details>

<details>
  <summary>Demo Day email list and template</summary>

Carbon Team list as of 9/16/2019: Abagail Hart/US/IBM@IBM, Akira
Sudoh/Japan/IBM@IBMJP, Alessandra Davila1/US/IBM@IBM, Alison
Joseph/Austin/IBM@IBMUS, Andrew Wang1/US/IBM@IBM, Anna
Gonzales/Austin/IBM@IBMUS, Chris Connors/Pittsburgh/IBM@IBMUS, Connor
Leech/US/IBM@IBM, DA Anguiano/US/IBM@IBM, Jan Child/US/IBM@IBM, Jean Ann
Servaas/US/IBM@IBM, Jeoff Wilks/Arlington/IBM@IBMUS, Jillian Howarth/US/IBM@IBM,
Josefina Noemi Mancilla/US/IBM@IBM, Joshua Black/Austin/IBM@IBMUS, Lauren
Rice/Austin/IBM@IBMUS, Matt Rosno/US/IBM@IBM, Robin Cannon/Austin/IBM@IBMUS,
Timothy W Egan/Austin/IBM@IBMUS, Tyler R Tate/Austin/IBM@IBMUS, Vincent Patrick
Picone/US/IBM@IBM, Xiangjun Shi Trofimov/US/IBM@IBM,

Title: Carbon [Month] release demo day

Subject: This will be a review of the work completed at the end of the October
release cycle.

Link to Carbon October release planning:
https://github.com/carbon-design-system/carbon/wiki/Carbon-October-Release-Planning

Link to the Box note Agenda:
https://ibm.ent.box.com/notes/342752664012?v=demo-day-agenda-design-system

Please fill out a time slow with the topic and presenters before the meeting.

</details>

### Week 2: Project work

Checklist:

- [ ] Patch release on Monday

### Week 3: Project work

Checklist:

- [ ] Patch release on Monday
- [ ] Run mid-project playbacks on Thursday afternoon
  - Those invited should be the core team and relevant project stakeholders
    (reach out to project teams to figure out who those individuals are)

### Week 4: Pre-endgame planning

Checklist:

- [ ] Patch release on Monday
- [ ] Announce in core channel that code freeze is at the end of the week
- [ ] Reach out to teams and figure out critical dependencies that are
      ship/no-ship criteria
  - [ ] Document these in the endgame issue for the Monday task
- [ ] Create endgame issue and pin it to the Carbon repo by end of week

#### Templates

<details>
  <summary>Issue template</summary>

```md
Title: {Month} 20XX Endgame

This is the endgame schedule for our Month 20XX iteration, which includes the
following projects:

- [Project 1](#project-1)
- [Project 2](#project-2)
- [Project 3](#project-3)

## Schedule

- Endgame leader: @username
- Endgame sidekicks: @username (role), @username (role)
- XX/YY: Code freeze (EOD)
- XX/YY: Endgame done
- XX/YY: Expected release date

### Monday XX/YY

- [ ] Set endgame-specific branch protection rules
- [ ] Coordinate delivery or resolution of the following items:
  - [ ]
- [ ] Start code freeze (EOD)
  - [ ] Announce code freeze on final day before the endgame
  - [ ] Enable code freeze branch protection on relevant repos

### Tuesday XX/YY

- [ ] First Release Candidate cut
- [ ] Complete first round of smoke tests
- [ ] Share with Carbon Insiders for first round of testing

### Wednesday XX/YY

- [ ] Collect first round of feedback from Carbon Insiders (if available)
- [ ] Triage release-specific issues and bucket them into two categories:
  - [ ] Stop release
  - [ ] Ship with known issues
- [ ] Coordinate merging of bug fixes related to release
- [ ] Cut next Release Candidate, if applicable
  - [ ] Share newest release with Carbon Insiders for additional rounds of
        testing

### Thursday XX/YY

- [ ] Collect second round of feedback from Carbon Insiders (if available)
- [ ] Coordinate merging of bug fixes related to release
- [ ] Cut next Release Candidate, if applicable
  - [ ] Share newest release with Carbon Insiders for additional rounds of
        testing

### Friday XX/YY

- [ ] Collect final round of feedback from Carbon Insiders (if available)
- [ ] Run final smoke tests on release
- [ ] Make determination to release on following Monday

### Monday XX/YY

- [ ] Release Monday morning
- [ ] Coordinate release communications on Slack and Twitter
- [ ] Summarize top-level release notes for next blog post
```

</details>

### Week 5: The endgame

Checklist:

- [ ] Enforce code freeze
- [ ] Make sure to follow along with steps outlined in endgame issue
- [ ] Collect feedback from teams for critical dates
- [ ] Follow-up and help to coordinate delivery of items
- [ ] Make determination on ship/no-ship together with endgame team
- [ ] Have teams comment project outcomes in endgame issue (set hard deadline)

### Week 6: Release and planning

Checklist:

- [ ] Release on Monday under `next` tag
- [ ] Switch to `latest` on Tuesday
- [ ] Open website PR to update our
      [What's new page](https://www.carbondesignsystem.com/updates/whats-new)
      with `latest` changelog
- [ ] Run release demo (1 hour)
  - Those invited should be direct team and board members
- [ ] Run release retro (1 - 2 hours)
  - Those invited should be direct team members
  - [ ] Summarize retro discussion in our
        [ongoing doc](https://ibm.box.com/s/hr2zvaojw77l2940c0rdefmz1fde1evg)
- [ ] Participate in release planning for next cycle

## Releases

As part of the endgame process, the endgame team will faciliate the following
types of releases:

| Release type                                     | Description                                                             | Semver bump | Frequency                                          |
| ------------------------------------------------ | ----------------------------------------------------------------------- | ----------- | -------------------------------------------------- |
| [Hotfix](#hotfix-releases)                       | Fix severity level 1 issues with large user-facing impact               | `patch`     | On demand                                          |
| [Patch](#patch-releases)                         | Batched fixes to packages with varying degrees of severity and priority | `patch`     | Weekly                                             |
| [Release Candidate](#release-candidate-releases) | Features and fixes that will be included in minor release               | `preminor`  | Typically 6 weeks, as needed before minor release  |
| [Minor](#minor-releases)                         | Features and fixes to packages                                          | `minor`     | Typically 6 weeks, occasionally on-demand          |
| [Major](#major-releases)                         | Large or semver-incompatible changes to the design system               | `major`     | Typically 6 months to 1 year, announced in advance |

The Carbon team distributes these releases under two channels:

<!--
Inspiration for copy and terminology comes from Google Chrome:
https://support.google.com/chrome/a/answer/9027636?hl=en
-->

- Nightly
  - Users on the Nightly channel get a 4 to 6 week preview of what's coming to
    the Stable version of the Carbon Design System
  - The Nightly channel is updated daily and includes features and fixes the day
    after they're merged into the codebase
  - Users on the Nightly channel can discover possible issues with a release,
    giving you time to address the issues before the release is rolled into the
    Stable channel
  - Users on the Nightly channel may discover issues with the release and are
    priority support to help resolve those issues
- Stable
  - The Stable channel is fully tested by the Carbon Design System team and
    should be used by most product teams
  - This channel is updated weekly for `patch` releases (when applicable), and
    every 4 to 6 weeks for `minor` releases

### Hotfix releases

A hotfix release is triggered by a bugfix that was introduced into the codebase
that was high severity (2 or higher) and includes any of the following criteria:

- Impacts a large number of product-facing users
  - An example of this would be that a component is rendered in-operable
- Impacts a large number of direct consumers
  - An example of this would be that a broken package build was published

Hotfixes are published under the `patch` semver range and can be published at
any point in the endgame process.

#### Publishing steps

Same as patch release steps.

### Patch releases

A patch release is scheduled as a weekly update to batch bug fixes to the
project. It can also be created on-demand outside of this weekly schedule,
although these situations should be uncommon.

A `patch` release will contain changes to the codebase that fall under the
following categories:

- A bug fix to an existing piece of code
- Content or documentation updates
- Refactoring of existing code while supporting the same public API and not
  changing in behavior

The release may contain other types of software changes, however the one type of
update that is not shipped is the addition of functionality that does not
already exist in the project. These updates are reserved for
[minor releases](#minor-releases).

#### Publishing steps

1. From the root of your directory, checkout `master` and pull the latest
   upstream.
2. Run `./packages/cli/bin/carbon-cli.js release patch`

   - You will see the terminal do a few things: get the latest tag, find the
     next version to bump, create a branch for the release, and begin
     cherry-picking PRs. The most important thing to note when cherry-picking
     PRs is that we do not want to bring over `feat`, as this would be a
     breaking change for a [`minor`](#minor-releases) release.

   - If the PR commit does not follow commit syntax, the terminal will prompt
     you something similar to:

     ```bash
     ? Should we include commit: 2953c461a Non-commit syntax message here
     ```

     Type `y` to include it in the patch release or `n` to exclude it. If it's
     not clear right off the bat, you can find the merged PR by its number and
     look through it to see if it includes new features or not.

   - If you get a prompt that says:
     ```bash
     ? Applying the commit XXXXXX lead to a conflict. Please fix the conflict and then confirm to proceed. (y/N)
     ```
     Open a new tab in your terminal. You can view the changes by running
     `git status`. Run `git add -A`. Then run `git cherry-pick --continue`. Once
     you see that the changes have been committed, go back to your original
     terminal tab, where we are releasing. Type `y` in response to the prompt
     and continue.
   - If you get an error because a commit message is too long, run
     `git commit --no-verify`

3. Once the commits have been cherry-picked, you'll be prompted with something
   like:

   ```bash
   Changes:
    - carbon-components: 10.4.1 => 10.4.2
    - @carbon/elements: 10.4.0 => 10.4.1
    - @carbon/icons-angular: 10.4.0 => 10.4.1
    - @carbon/icons-handlebars: 10.4.0 => 10.4.1
    - @carbon/icons-react: 10.4.1 => 10.4.2
    - @carbon/icons-vue: 10.4.0 => 10.4.1
    - @carbon/icons: 10.4.0 => 10.4.1
    - carbon-components-react: 7.4.1 => 7.4.2
    - @carbon/sketch: 10.4.0 => 10.4.1 (private)

   ? Are you sure you want to create these versions? (ynH)
   ```

   You should inspect the list of changed packages to make sure they align with
   the commits you cherry-picked over. If something looks off, feel free to stop
   this command and figure out what is going on before starting again.

   If everything looks good, you can enter in `y` for `Yes` and `lerna` will
   handle versioning the corresponding packages.

4. Once that's done, you should create a Pull Request in Draft state and make
   sure **not** to merge it. Our goal with the Pull Request is to do a final
   sanity check for CI checks, verify preview links work as expected, and get
   final reviews from the endgame team for the release. _Note: Make sure to
   specify which packages are being updated for your reviewers._

5. Once everything is green, review the pull request. Make sure there are no
   commits labeled `feat` as the patch release should only be for bug fixes,
   content updates, or refactoring existing code. Double check that the
   `package.json` versions are updated correctly by verifying the green
   (updated) version numbers are an incremental increase to the red (deleted)
   version numbers. If everything is correct, **close** the draft Pull Request.

6. On your machine, you should then follow the following steps to publish to
   `next`:

   - From your **PR branch**, run
     `yarn lerna publish from-package --dist-tag next` to publish all packages
     under the `next` tag
   - After publishing to `next`, run the smoke tests that we have listed
     [here](#testing) with the published packages

7. If everything looks good to go, checkout `master` and pull the latest
   upstream. Then you should go through each of the updated packages and add the
   `latest` tag using the command:
   `npm dist-tag add package-name@vX.Y.Z latest`. For example, if you just
   released `10.6.1` under `next`, this would look like
   `npm dist-tag add carbon-components@10.6.1 latest`.

   - Manually check to see that the `latest` tags were updated for the packages
     correctly by going to [`npm`](https://www.npmjs.com), searching the
     packages, viewing the versions and making sure the `latest` version matches
     the version you just released.

### Release Candidate releases

​ Before our minor releases, we cut Release Candidates a week in advance to
sanity check our code. ​

#### Publishing steps

1. Checkout `master`, and pull the latest upstream
2. Create a branch for your release candidate PR following the convention
   `chore/release-vX.Y.Z-rc.X`. For example, if we’re cutting the first RC for
   `v10.6` the branch would be `chore/release-v10.6.0-rc.0`, the second RC would
   be `chore/release-v10.6.0-rc.1` and so on.
3. Once you’ve created the branch, run
   `yarn lerna version preminor --exact --preid rc --no-push --no-git-tag-version -m 'chore(release): update package versions'`
4. Open a PR with the changes, and merge after approval.
5. Once the PR is merged, run the following scripts from `master` to publish the
   RC under the `next` tag: ​

   ```
   yarn clean
   yarn install --offline
   yarn build
   yarn lerna publish from-package --dist-tag next
   ```

6. Manually check to see that the `next` tag was updated for the packages
   correctly by going to [`npm`](https://www.npmjs.com), searching the packages,
   viewing the versions and making sure the `next` version matches the version
   you just released.

### Minor releases

A minor release represents the addition of functionality and bug fixes to the
codebase. Typically, they are released on a 4 to 6 week cadence. However, they
can be released on-demand in specific circumstances.

#### Publishing steps

1. Checkout `master`, and pull the latest upstream
2. From the root directory, run `./packages/cli/bin/carbon-cli.js release minor`

   - This will checkout the latest tag, find the next version for you to bump,
     create a new branch for your release, and reset your project state before
     prompting you to create the next version.
   - You should see a confirmation dialog similar to the following:

     ```bash
     Changes:
      - carbon-components: 10.5.0 => 10.6.0
      - @carbon/elements: 10.5.0 => 10.6.0
      - @carbon/icons-angular: 10.5.0 => 10.6.0
      - @carbon/icons-handlebars: 10.5.0 => 10.6.0
      - @carbon/icons-react: 10.5.0 => 10.6.0
      - @carbon/icons-vue: 10.5.0 => 10.6.0
      - @carbon/icons: 10.5.0 => 10.6.0
      - carbon-components-react: 7.5.0 => 7.6.0
      - @carbon/sketch: 10.5.0 => 10.6.0 (private)

     ? Are you sure you want to create these versions? (ynH)
     ```

   - If everything looks good, you can enter in `y` for `Yes` and `lerna` will
     handle versioning the corresponding packages.

3. After the package versions have been created, you'll be prompted
   `The next step will be to manually create a Pull Request for this branch`.
   Simply push your changes and open the PR. Be sure your commit message reads
   `chore(release): update package versions`
4. Once your PR is approved and merged, checkout `master`, pull the latest
   upstream and run:

   ```
   yarn clean
   yarn install --offline
   yarn build
   ```

5. Then, update `next` by running
   `./packages/cli/bin/carbon-cli.js publish vX.Y.Z`.

6. At the end, the terminal will print out raw markdown for the changelog. Copy
   the markdown, and update the
   [release](https://github.com/carbon-design-system/carbon/releases) changelog
   for the version. Make sure the title matches the existing tag, `vX.Y.Z`.
7. Manually check to see that the `next` tag was updated for the packages
   correctly by going to [`npm`](https://www.npmjs.com), searching the packages,
   viewing the versions and making sure the `next` version matches the version
   you just released.

8. When you're ready to update `latest`, run
   `npm dist-tag add package-name@X.Y.Z latest` for each of the updated
   packages. For example, when releasing `10.6`, this would look like:

   ```bash
   npm dist-tag add carbon-components@10.6.0 latest
   npm dist-tag add carbon-components-react@7.6.0 latest
   npm dist-tag add @carbon/elements@10.6.0 latest
   npm dist-tag add @carbon/grid@10.6.0 latest
   npm dist-tag add @carbon/icons-handlebars@10.6.0 latest
   npm dist-tag add @carbon/icons-react@10.6.0 latest
   npm dist-tag add @carbon/icons-vue@10.6.0 latest
   npm dist-tag add @carbon/icons@10.6.0 latest
   npm dist-tag add @carbon/layout@10.5.0 latest
   npm dist-tag add @carbon/type@10.5.0 latest
   npm dist-tag add @carbon/themes@10.6.0 latest
   ```

9. Like before, manually check to see that the `latest` tags were updated for
   the packages correctly by going to [`npm`](https://www.npmjs.com), searching
   the packages, viewing the versions and making sure the `latest` version
   matches the version you just released.

### Major releases

A major release represents the addition of semver-incompatible changes to the
project, and are only expected to occur every 6 months to a year. These releases
will be announced in advance, and migration strategies and support will be made
available to assist in transitioning between versions.

#### Publishing steps

## Testing

Before shipping a release of the Carbon Design System, we need to run through
the following testing scenarios:

- [ ] Trigger update for release under our own projects, namely:
  - [ ] `carbon-website`
  - [ ] `gatsby-theme-carbon`
- [ ] React smoke tests
  - [ ] `create-react-app`

### Procedures

#### `create-react-app`

## FAQ

#### Making sure your environment is consistent with `upstream`

```bash
yarn clean && \
yarn install --offline && \
yarn build
```
