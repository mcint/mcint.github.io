# Methods

I tried pelican on github pages. I have too much past frustration with jekyll
to want to set up ruby and gems again locally just to publish a static site. I
would rather first write my own bash and make site generator.

# This site

I'm using MkDocs, locally running it with `poetry run` `mkdocs
serve`.

I edit (and preview) on personal computer with github keys, and push to github
for publishing to Pages.

# Ideal workflow

Easy writing and deployment. MkDocs's serve, with a jupyter notebook to writing
updates. Maybe autocommitting, but publish as I write, and close access to
powerful tools like the python ecosystem.

## Building it further

I should make this a checklist, or a table for comparisons. A table would be
nice, I can even list the strength of each framework in its own terms and
consider the cartesian product of qualities I've loved with solutions on offer.


# Frustrations, observations
Taking inspiration from NVC (Non-Violent Communication), I'm seeking 1)
Observations, to uncover 2) Feelings, to assess 3) Needs, to arrive at 
4) Requests for the tools and workflows I'll choose to use (OFNR).

## Site generators
- jekyll
    - ruby, gem. installation, upgrades, slow painful compile to get the tool,
      sudo for text processing.
- mkdocs
    - TOC header levels. 1# expected as page title, and for upper out of
      2-level header visibility. 3rd level hidden.
    - 4-indent for nested lists (not just 2, or 1). Possibly configurable,
      check mkdocs.yml docs.
    - nice if:
        - headers, in-page, had static fragment links. Only TOC renders them.

## Hosting provider
- Github Pages
    - \+ good uptime
    - \- slow to deploy
    - \- requires trusted computer, github keys, git add-commit-push process.
- Self-host 
    - \+ faster iteration. preview while editing. live site, or dev site
    - \- uptime, risk of downtime. site longevity. domain.

makes me want to build a site that can output to run on gh-pages, but that I
edit primarily on personal site. under consideration.


