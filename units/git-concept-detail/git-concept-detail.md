---
# from style yaml - begin
marp: true
theme: dataplant_marp-theme
paginate: true
headingDivider: 
  - 1
  - 2
footer: '
<a href="https://nfdi4plants.org">
  <img id="footer-img1" src="../../images/_logos/DataPLANT/DataPLANT_logo_square_bg_transparent.svg">
</a>
<a href="https://ceplas.eu">
  <img id="footer-img2" src="../../images/_logos/CEPLAS/CEPLAS_Icon.jpeg">
</a>
<a href="https://creativecommons.org/licenses/by/4.0/">
  <img id="footer-img3" src="../../images/_logos/CreativeCommons/cc-by.svg">
</a>'
style: |
  footer {
    height: 30px;
    padding: 10px;
    bottom: 00px;
  }
  #footer-img1 {
      height: 30px;
      padding-left: 0px;
  }
  #footer-img2 {
      height: 30px;
      padding-left: 20px;
      opacity: 0.5;
  }
  #footer-img3 {
      height: 20px;
      padding-left: 20px;
      opacity: 0.5;
  }
# from style yaml - end
author: ['Dominik Brilhaus']
author_orcid: ['https://orcid.org/0000-0001-9021-3197']
author_github: ['brilator']
license: ['[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/)']
title: ['Git concept detail']
duration_minutes: ['5']
date: ['2023-03-16']
status: ['draft']
headingDivider: ['1']
---
<!-- headingDivider: 1 -->

# Concept of Git and Git-based platforms



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/title-Git-concept-detail.md -->
<!-- ################# -->


# Cloud Services

![bg right:50% w:800](../../images/DataSharing_Cloud_img6.png)

<span style="color:#B4CE82">✓ Documents</span>  
<span style="color:#B4CE82">✓ Small data</span>  
<span style="color:#B4CE82">✓ Presentations</span>  

<span style="color:#c21f3a">X  Code</span>  
<span style="color:#c21f3a">X  Data analytical projects</span>  
<span style="color:#c21f3a">X  Big (“raw”) data</span>  


<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/cloud-services.md -->
<!-- ################# -->


# Git and Git platforms

![bg right:50% w:800](../../images/DataSharing_Git_img1.png)

<span style="color:#F9CD69">∼ Documents</span>
<span style="color:#B4CE82">✓ Small data</span>  
<span style="color:#F9CD69">∼ Presentations</span>

<span style="color:#B4CE82">✓✓ Code</span>
<span style="color:#B4CE82">✓✓ Data analytical projects</span>
<span style="color:#F9CD69">∼ Big (“raw”) data</span>



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/Git-and-Git-platforms.md -->
<!-- ################# -->


# Why Git? ≈> Why code?

- Save time
- Avoid doing repetitive tasks “by hand”
- Reuse scripts, analyses, pipelines
- Reproduce results


<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/Git-why.md -->
<!-- ################# -->


# A simple example: RNASeq project

![w:900](../../images/Git_RNASeq_Example_img1.png)

# A simple example: RNASeq project

![w:900](../../images/Git_RNASeq_Example_img2.png)

# A simple example: RNASeq project

![w:900](../../images/Git_RNASeq_Example_img3.png)

# A simple example: RNASeq project

![w:900](../../images/Git_RNASeq_Example_img4.png)

# A simple example: RNASeq project

![w:900](../../images/Git_RNASeq_Example_img5.png)



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/example-project.md -->
<!-- ################# -->


# Take snapshots of your code work…
(... as long as it works)

![w:900](../../images/Git_RNASeq_Example_img6.png)

# Take snapshots of your code work…
(... as long as it works)

![w:900](../../images/Git_RNASeq_Example_img7.png)


<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/Git-snapshots.md -->
<!-- ################# -->


# Scenario 1: More data

![w:900](../../images/Git_RNASeq_Example_img8.png)

# Scenario 1: More data

![w:900](../../images/Git_RNASeq_Example_img9.png)

# Scenario 1: More data

![w:900](../../images/Git_RNASeq_Example_img10.png)



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/example-project-moreData.md -->
<!-- ################# -->


# Let Git track changes and keep things clean

![w:900](../../images/Git_RNASeq_Example_img11.png)



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/Git-track-changes.md -->
<!-- ################# -->


# Scenario 2: Pipeline breaks

![w:900](../../images/Git_RNASeq_Example_img12.png)



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/example-project-break.md -->
<!-- ################# -->


# Revert to snapshot

![w:900](../../images/Git_RNASeq_Example_img13.png)


<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/Git-revert.md -->
<!-- ################# -->


# Scenario 3: New project, same type of data and analysis <!-- fit -->

![w:900](../../images/Git_RNASeq_Example_img14.png)

# Scenario 3: New project, same type of data and analysis <!-- fit -->

![w:900](../../images/Git_RNASeq_Example_img15.png)



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/example-project-reuse.md -->
<!-- ################# -->


# Re-use code

![w:900](../../images/Git_RNASeq_ReuseCode_img1.png)

# Re-use code

![w:900](../../images/Git_RNASeq_ReuseCode_img2.png)

# Re-use code – People have done this

![w:900](../../images/Git_RNASeq_ReuseCode_img3.png)

# Re-use code – People have done this

![w:900](../../images/Git_RNASeq_ReuseCode_img4.png)



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/Git-reuse.md -->
<!-- ################# -->


# Re-use code – Link and contribute

![w:900](../../images/Git_RNASeq_ReuseCode_img5.png)



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/Git-contribute.md -->
<!-- ################# -->


# Git: summary

- Version control system
- Git “repository” = a central data package (directory)
- Allows to track changes to any file in the repository
  - **What** was changed
  - **When** was it changed
  - By **whom** was it changed
  - **Why** was it changed?



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/Git-summary.md -->
<!-- ################# -->


# GitHub and GitLab

- A well-documented cloud environment
- Active syncing
- Not automatically synced
- Non-automated version control
- You have the control what changes to track and what to sync
- Time machine to go back to older versions



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/GitHub-GitLab.md -->
<!-- ################# -->


# GitHub and Gitlab team projects

Simplifies concurrent work & merging changes
- Online service to host our projects
- Share code with other developers
- Others can download our projects, work on and contribute to them
- They can upload their changes and merge them with the main project



<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/team-projects.md -->
<!-- ################# -->


# Cloud vs. Git

![w:1000](../../images/Git_cloud_comparison.png)


<!-- ################# -->
<!-- Source to slide(s) above -->
<!-- bricks/cloud-vs-Git.md -->
<!-- ################# -->

