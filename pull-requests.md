# Pull requests (PRs)

This is a PR style guide for working on M&S code.

## Why we do pull requests on M&S

- It's good practice to have a second opinion
- Even if pair-programming, you need a third person to merge
- It's good to spread knowledge and socialise changes amongst others
- It can help involve other people (via email, GitHub notifications etc).
  We can even 'mention' specific people or teams with `@name` syntax

## Cautionary notes

- Don't use PRs for architectural review - do this before raising the
  pull request
- Don't rely on someone else to spot and merge your PR - it's your job
  to find a reviewer and get the code merged
- Kanban work-in-progress limits, automated tools and other things can help
  you spot when PRs are piling up and need attention
- A PR doesn't have to be all the work. It should be possible to make the
  change live. It's okay to have follow-up PRs for a feature. For instance,
  an initial PR might introduce a feature flag behind which the feature can
  be developed

## Guidance for each step

If you are not sure how to do any of this, please feel free to ask for
help.

### Opening a request

- Before opening the PR, make sure you're up to date with `master` so
  that your changes are easier to merge
- The title and description should help the reviewer. Make the title
  succinct and descriptive, and then add detail in the description
- The description should summarise your changes and include useful links.
  For example, a JIRA ticket, support ticket, or related PR. If the changes
  involve frontend code, we love screenshots showing before and after. Other
  good things might be a WebPageTest video
- When raising a PR, the title and description are emailed to those
  following the repo. Any later changes are not emailed, so it's worth
  spending a bit of time getting it right at the point of raising the PR.
- It is worth explaining any contentious changes, and any testing that you
  have already done

Note: The canonical description of changes should always be in the
individual commits. PRs are an artefact of GitHub, and we would lose that
data if we switched away. Please refer to the [commit message styleguide](/git.md#commit-messages).

### Reviewing a request

#### Guidelines for review

- Take time to review a PR; the review  stage is as important as writing
  the code in the first place
- If you're not sure how the individual wants their request reviewed, ask
  them before starting - they may prefer some of the feedback in person or
  while pairing (especially if they're less experienced)
- Comments on PRs should include positive feedback as well as developmental
  feedback. If the code is good, or solves something in a clever way, *say so*.
  Call out individual bits of quality to:

  - signpost better practice for others
  - reward the person submitting the request

- Be explicit what, if anything, is a blocker

#### Communicate with others who may consider reviewing the PR

- If you're going to discuss some issues offline, please comment as such in
  the PR so that no-one merges it in the meantime. When conversation has
  taken place elsewhere, summarise the conversation as a comment on the PR
  for the benefit of others
- If you look at a PR but don't feel comfortable merging it, please say what
  you've looked at. Then other reviewers know the request hasn't been
  properly reviewed
- If you're committed to reviewing the request through to merging or
  closing, assign the PR to yourself

#### Helpful things to consider while reviewing

- Try running the code - even if the tests pass it might have bugs
- Consider security when reviewing code, particularly where there is user
  input. The [basic security guidance](basic-security.md) might help
- Remember that a PR does not have to solve the whole problem. If it adds
  value on its own it is better to merge now rather than wait for the rest
  of the changes required.
- Always comment on individual lines in the full-file diff view, not on a
  commit page because GitHub loses them if you rebase
- Ensure that any relevant documentation (`README` files, things in the
  `doc` folder) is up to date with the changes

### Addressing comments

- Any comments flagged as blocking should have a response. This includes
  spelling or grammatical errors in documentation
- If you're changing something minor in an existing commit, amend the
  existing commit. Please ask for help if you don't know how to do this
- Major changes should happen in a separate commit. Be sure that when
  addressing changes you follow existing commit guidelines. In particular,
  include a good commit message.
- Explicitly comment that all relevant comments have been addressed to
  notify any watchers - you don't need to do this on a per-comment basis
- Refactoring can and should happen in follow-up separate pull request --
  it shouldn't ever be blocker
- Conversations on a PR should be rolled into the existing or new commits.
  Github and pull-requests are temporary - a commit message is forever

## 'Done'

'Done' doesn't just come when the code is merged. Features should not be
considered delivered until they're in production, and it's the
responsibility of the developer who wrote the code to ensure their work is
deployed in a timely fashion.

## Further reading

- [Anna Shipman](https://github.com/annashipman) has written a useful blog post about [how to raise a good pull request](http://www.annashipman.co.uk/jfdi/good-pull-requests.html)
- A great example of [a good pull request](https://github.com/alphagov/frontend/pull/784) raised by [Alice Bartlett](https://github.com/alicebartlett)
