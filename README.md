# Imprecise Probabilistic Machine Learning

![IPML](course-logo.png)

> “There are known knowns. There are known unknowns. But there are also unknown unknowns—things we do not yet realize we do not know.” — Donald Rumsfeld (2002)

This repository holds the course website and material for **Imprecise
Probabilistic Machine Learning (IPML)**.

**Website: <https://muandet-lab.github.io/ipml-course/>**

| | |
|---|---|
| Current offering | [Winter Semester 2026/27](https://muandet-lab.github.io/ipml-course/2026-2027/) |
| Past offerings | [Winter Semester 2025/26](https://muandet-lab.github.io/ipml-course/2025-2026/) |
| All offerings | [Course archive](https://muandet-lab.github.io/ipml-course/archive/) |
| Reading list | [References](https://muandet-lab.github.io/ipml-course/references/) |

## How the repository is organised

The site is a single permanent [Jekyll](https://jekyllrb.com/) site in which
every offering of the course lives under its own stable subdirectory, so URLs
stay citable years later and an old semester is never overwritten by a newer
one.

```
ipml-course/
├── _config.yml              # site settings + per-offering front matter defaults
├── _data/
│   ├── offerings.yml        # every offering; drives the home page and /archive/
│   ├── nav.yml              # navigation (per-offering + permanent items)
│   └── people.yml           # instructors and teaching assistants
├── _layouts/  _includes/  _sass/  _css/  _images/
│
├── _lectures/<offering>/    # one file per lecture (title, tl;dr, slides, readings)
├── _assignments/<offering>/ # one file per exercise sheet
├── _events/<offering>/      # holidays, exams and other dated events
├── _announcements/          # manual announcements
│
├── 2026-2027/               # current offering: pages + slides/
├── 2025-2026/               # archived offering: pages + slides/ + exercises/
│
├── index.md                 # permanent course overview
├── archive.md               # /archive/ — generated from _data/offerings.yml
└── references.md            # /references/ — permanent reading list
```

Content that belongs to a semester (slides, worksheets, dates, room numbers)
lives under that semester's folder. Content that outlives a semester (the course
description and the reading list) lives at the top level.

## Common tasks

**Publish the slides for a lecture.** Drop the PDF into
`<offering>/slides/` and add a `links:` entry to the matching file in
`_lectures/<offering>/`:

```yaml
links:
    - url: /2026-2027/slides/lecture-01-introduction.pdf
      name: slides
```

**Put a lecture on the schedule.** Add `date:` and `scheduled: true` to the
lecture file. Items without `scheduled: true` are listed on the Lectures page
but left off the Schedule — Jekyll gives every undated document the build time
as its date, so the flag, not the date, decides.

**Release an exercise sheet.** Add a file under `_assignments/<offering>/`
following `_assignments/2025-2026/01_worksheet-part-i.md`, and put the PDF in
`<offering>/exercises/`.

**Post an announcement.** Add a dated file to `_announcements/` with
`offering: "<offering>"` in its front matter.

## Starting a new offering

1. Copy the newest offering folder, e.g. `cp -r 2026-2027 2027-2028`, and update
   the `permalink:` in each page inside it.
2. Copy `_lectures/2026-2027/` to `_lectures/2027-2028/` and update `offering:`
   in each file (likewise for `_assignments/` and `_events/` if needed).
3. Add a `defaults` block for the new folder in `_config.yml`.
4. Add an entry at the top of `_data/offerings.yml` and move `current: true`
   to it — in both `_config.yml` and `offerings.yml`.

The previous offering then keeps working exactly as it was, and automatically
gains an "archived offering" banner linking to the new one.

## Running the site locally

Requires Ruby (3.1+) and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000/ipml-course/>.

## Deployment

Pushes to `main` are built and published by the GitHub Actions workflow in
[`.github/workflows/pages.yml`](.github/workflows/pages.yml). This requires
**Settings → Pages → Build and deployment → Source** to be set to
**GitHub Actions** once.

## Contributing resources

If you are aware of a relevant resource that should be listed in
[`references.md`](references.md) (e.g. your own work), please open a pull
request or contact us by [email](mailto:muandet@cispa.de?subject=IPML:%20Missing%20Resources).

## Acknowledgement

The website is based on the
[jekyll-course-website-template](https://github.com/kazemnejad/jekyll-course-website-template)
by Amirhossein Kazemnejad (MIT licensed, see [TEMPLATE-LICENSE](TEMPLATE-LICENSE)),
which in turn is based on [svmiller/course-website](https://github.com/svmiller/course-website).
