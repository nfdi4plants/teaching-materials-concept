# Contributing

## Repository rules for collaborators

### Pull requests

- Do not push into the main branch.  
- Use branches or forks and make pull requests.  
- Make sure that tasks / files modified of different contributors do not overlap to avoid merge conflicts.
- Assign reviewer(s).  
- Merge PR after positive review / approval.  
- Delete local and remote branch after merging. (optional)
- Minimize road blocks with "hanging" PRs.  
- Create small "actionable" PRs.

### Issues

- Short title (as short as possible).
- Concise, non-cryptic description.
- As small as possible, actionable, checkable
- Single issues
  - Bundle single steps towards one outcome via task lists within one issue.
  - Bundle multiple ("independent") issues into a milestone.
- Use labels to categorize.
- Add the issue to the project board [TeachingMaterial-ProjectBoard](https://github.com/orgs/nfdi4plants/projects/1)
- Self-assign ("pick from board") unless discussed in meeting / in person.
- When somebody is already assigned only assign as well when discussed with the first assignee.  

### Project Board

- The project board used is [TeachingMaterial-ProjectBoard](https://github.com/orgs/nfdi4plants/projects/1)
- Create issues in the project board.
- Use milestones.
- See above.

<br>

## Repository Overview

folder | content
--- | ---
.vscode | settings relevant for vs code (extensions)
bricks | individual bricks that can be combined into units [see brick-types](#brick-types)
units | units that can be combined into disseminations [see unit-types](#unit-types)
disseminations | disseminations that can be used for an event [see dissemination-types](#dissemination-types)
images | images
style | css-theme(s) for marp slides

<br>


### Brick types

- markdown slides
- docs
- videos
- ...

### Unit types

type | description | typical layout(s)
--- | --- | ---
lesson | convey knowledge | slides
exercise | educational, learn from (inter)active practice | slides, docs
demo | demonstrate tool, showcase skill | slides, (video, screencast)
feedback | collect participant feedback | slides
tutorial | (self-)guided tutorial | slides, docs, (video, screencast)
article | written out text (knowledge base) | docs
handout | Literally a (few-pager) handout to give away| docs?
checklist | Provides an overview of items to be considered for a specific purpose | docs, slides

### Dissemination types

Dissemination type | Target audience | Example
---------|----------|---------
One-on-one / consulting | PIs, CIs | phone/zoom call during proposal, funding, acquiring / associating a (new/existing) SFB
Train-the-trainer | Data Stewards | Onboarding of new DataPLANT data stewards
Training (practical) | all (DataPLANT) users | Training on a (specific) DataPLANT tool(s)
Teaching (theory + practical) | Students/PhD/PostDoc | PhD course on good data management practice
Workshop | all (DataPLANT) users | Bring your own data (and build your ARC)

<br>

## File naming convention

### Bricks
- short title with content information

### Units
- "unit-type_*consecutive number*_specifier"

<br>

## Improving reusability

- Small packages
  - The smaller ~ the more re-usable
  - The smaller ~ the easier to Git collaborate without merge conflicts
- Metadata header (see below)
- Markdown (slides)
  - YAML header for metadata (context)
  - formulated text can easily be converted into slide notes
  - see tutorial on Marp slides
- Distinguish "figures" from "slides"
  - figures can be used for multiple output formats (website/knowledge based, slides, tutorials, handouts)
  - The folder `images` holds image (*.svg, *.png) files (not slides) or the original source file (.pptx, .drawio.svg) used to create the image file(s). 
- If powerpoint is used to create a figure
  - the pptx stored in `images` is supposed to be a file of only a single slide or slide sequence (i.e. consecutive slides, where one image builds on the previous)
  - the name of the resulting figure file (e.g. "FAIRprinciples.png") MUST be aligned with the source file (e.g. "FAIRprinciples.pptx")
    - a consecutive number is suffixed to images from slide sequences (e.g. "FAIRprinciples_seq1.png", "FAIRprinciples_seq2.png")

<br>

## Figure design

### Design

- pure figures
  - no caption
  - no link

- image directory: reusable, named, single image files

- copyright, licenses
  - list links to all external figures in images/README.md

### Tools

- powerpoint
- draw.io (e.g. VS code extension)

### Output formats

1. svg (preferred)
2. png
3. jpeg
4. pdf

<br>

## Slide Design

Currently (Feb 23), slides in this repo are built from markdown files using the [marpit](https://marpit.marp.app/) framework. For technical guide see [tutorial_003_IntroMarpSlides.md](./units/to_be_split_into_bricks/tutorial_003_IntroMarpSlides.md).

There are some technical flavors that let MARP interpret the slide design differently.
To avoid incompatibilities when combining multiple slide decks into one:

1. add the following to your YAML header
```yaml
---
marp: true
theme: dataplant_marp-theme
headingDivider: 
  - 1
  - 2
---
```
2. This makes sure that slides are "cut" at level 1 (h1, `#`) and level 2 (h2, `##`) headers. Note, also a line with '---' below the yaml header will break slides.
3. Use only "scoped" (CSS) directives
   1. Via the underscore mechanism, e.g. `<!-- _paginate: false -->`
   2. Via html tag 
       ```html
       <style scoped>' (instead) of <style>. Otherwise the adapted style applies to all slides (of a combined slide deck).
       ```

<br>

## "File specs"

- __bricks__, __units__ and __disseminations__ are **markdown files** (file extension: .md)
  - they can be interpreted and rendered *as-is* by e.g. VS Code (extensions), GitHub, marp-cli, etc
  - they contain a suitable yaml header  
- unitpaths and disseminationpaths
  - they point to the relative paths of bricks or units in the desired order
  - they are interpreted by a script (currently: compile_marp_slides.sh), which compiles the listed bricks and units into a unit or dissemination
  - they MAY contain a suitable yaml header
  - they MAY contain empty lines and comments (lines starting with `#`)

### Training material metadata header

- We use YAML metadata header aiming to provide FAIR training material (for details, see below in the file specs).
- Inspired by <https://doi.org/10.1371/journal.pcbi.1007854.t002>
- Why YAML (or YML)?
  - hidden from rendered markdown
  - machine-readable (think database, keywords, etc.)
#### YAML headers  

- __brick level__ metadata  

    ```yaml
    # Slide-related yaml  
    marp: true  
    theme: dataplant_marp-theme  
    # Training yaml  
    layout: slides  
    title: "brick_dummy"  
    contributor_name:  
    - contributor1  
    - contributor2  # this is how to add multiple values  
    contributor_orcid:  
    contributor_github:  
    images_used:  
    citation:  
    license:  
    description:  
    keywords:  
    comments:  
    date: YYYY-MM-DD  
    status: empty #or draft or ready  
    ```  

- additional __unit level__ metadata  

    ```yaml
    learning outcomes:
    skills:
    abilities:
    requirements:
    required resources:
    teaching mode:
    duration_minutes:
    links and references:
    ```

- additional __dissemination level__ metadata to bricks and unit level metadata  

    ```yaml
    target audience:
    ```

Note, if a dissemination is built only from bricks, the dissemination metadata should comprise all entries from bricks, units and disseminations. Similarly, if it is built only from units, it will already contain the bricks metadata as this will be inherited by the unit level metadata.

### Relative paths (to images)

Needs careful construction, especially when trying to compile across multiple folder (e.g. submodules).

1. Any link within a "source" file (brick, style, unitconfig, unitpath, etc.) **MUST** be a correct relative path.
    > Example
    > If a `brick.md` references an image at `../images/image.png`, the image **MUST** exist at `../images/image.png` relative to the `brick.md`
2. A unit folder **MUST** containt a `unitpath` and a `unitconfig` file.
3. The name of the compiled output is the same as the folder (e.g. a unit folder "dummy" will contain a "dummy.md" and a "dummy.pdf")
4. Bricks and images **MAY** be organized into subfolders of `bricks` and `images`, but it's probably safer to avoid this.

<br>


