# How we ship at One Algorithm

You get access to **the project you work on**, nothing else. Everything below is enforced by
GitHub, not by trust.

## 1. Work on a branch

```
git checkout -b short-description-of-change
# ...edit, commit...
git push -u origin short-description-of-change
```

You **cannot** push to a project's live branch (`main`, `master` or, on Gorband, `final-version`).
GitHub will refuse.

## 2. Open a pull request

Open a pull request from your branch into the live branch. Say in plain words what changed and why.

## 3. Automatic checks run

Every pull request is checked automatically:

- **Websites:** the site is built and up to 40 pages are opened on an iPhone, an Android phone and a
  desktop. It fails on any broken image, page that scrolls sideways, page error, or a "Save page as"
  folder committed by mistake.
- **Apps:** the app's own self-tests run.

A red check means fix it before asking for review. You can open the failing run and read exactly
which page and which problem.

## 4. Review and approval

One approval from Louis or Sahith is required. Nothing merges without it.

## 5. Release

Merging does **not** publish by itself on most projects. A preview link is built first; Louis or the
client approves what they see; then it goes live.

## Never do this

- **Never commit passwords, API keys or `.env` files.** GitHub blocks known key formats on push. If it
  blocks you, do not try to get around it — tell us.
- Never commit database dumps, saved web pages, or large files you did not make.
- Never paste client data into AI tools or public sites.

## Account requirements

Two-factor authentication must be on for your GitHub account.

Questions: Louis Rubino, lrubino@onealgorithm.com
