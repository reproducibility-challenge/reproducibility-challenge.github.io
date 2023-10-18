---
title: Announcing MLRC 2023
linktitle: Announcing MLRC 2023
toc: true
type: book
date: "2023-10-18T00:00:00+01:00"
draft: false

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

Every year since 2018, we have conducted the Machine Learning Reproducibility
Challenge (see previous years
[v1](https://www.cs.mcgill.ca/~jpineau/ICLR2018-ReproducibilityChallenge.html),
[v2](https://www.cs.mcgill.ca/~jpineau/ICLR2019-ReproducibilityChallenge.html),
[v3](https://reproducibility-challenge.github.io/neurips2019/),
[v4](https://reproducibility-challenge.github.io/neurips2019/),
[v5](https://paperswithcode.com/rc2021),
[v6](https://paperswithcode.com/rc2022)), which invites the ML community to
examine the reproducibility of existing, recently published papers in top
conferences. As we gear up to announce the seventh iteration of the challenge,
MLRC 2023, we would like to share our learnings from previous years and how we
plan to incorporate these lessons into the upcoming challenge.

## Retrospectives

Over the years, the ML Reproducibility Challenge has been largely aimed at
students beginning their journey in ML research as part of their ML coursework.
This provided an accessible entry point to ML research, allowing early career
researchers to participate and learn a full paper publication lifecycle - from
designing the research question to investigating the limits of a scientific
hypothesis to final publication acceptance. One of the success stories of this
approach was from the University of Amsterdam, which designed a course around
the challenge
([FACT AI](https://studiegids.uva.nl/xmlpages/page/2022-2023-en/search-course/course/99121)),
and consistently produced high quality reproducibility reports in the final
proceedings of the challenge. While the challenge is a valuable resource to ML
course instructors and early career ML researchers, we are eager for the
challenge to grow in scope and impact. More specifically, we want to encourage
ML researchers to contribute novel research that will improve scientific
practice and understanding in the field. We thus identified several shortcomings
of the current model following our retrospection of the submitted and accepted
papers in the challenge.

While the challenge is a valuable resource to ML course instructors and early
career ML researchers, we are eager for the challenge to grow in scope and
impact. More specifically, we want to encourage ML researchers to contribute
novel research that will improve scientific practice and understanding in the
field. We thus identified several shortcomings of the current model following
our retrospection of the submitted and accepted papers in the challenge.

### Reproducibility is not a binary outcome

The term “reproducibility” unfortunately comes with a baggage - whenever we talk
about a paper to be reproducible, the expectation is this binary property - yes
or no. However, the reality is way more nuanced: a paper presents multiple
hypotheses (claims) of varying importance to the central claim - which some of
them can be directly reproducible, others might not be; some of the claims may
even be limited in terms
[“generalisability”](https://dl.acm.org/doi/abs/10.5555/3546258.3546422).
Consequently, we consistently found the quality of the reports submitted to the
challenge fall into either of these two categories: a) making a sweeping claim
about reproducibility, or b) diving deep and constructing a holistic view of
reproducibility, replicability and generalisability of the claims presented in
the original paper. Not surprisingly, the latter cohort is always highly rated
by the reviewers and ends up more often in the accepted pool. From the
[2020 iteration](https://paperswithcode.com/rc2020/registration), we introduced
a Reproducibility Summary template to encourage participants to focus on the
central claims of the paper, and to mainly focus on this generalisability
aspect - results beyond the original paper. We found that introducing this
template helps the authors to focus more on these questions, thereby improving
their submission.

### Reproducibility is not about whether author’s code gives the same results

Thanks to the continued effort made by the ML community in terms of Checklists
and mandatory code submission policies, we now see >90% of papers accompanied by
their source code. This is a very promising progress regarding reproducibility
of the research in our field - the presence of code alleviates many questions
and issues regarding the implementation, thereby facilitating exact
reproducibility. Inadvertently, this also resulted in many MLRC submissions
where authors only run the provided code and compare the numbers. While these
contributions measure replicability, they are not strong research contributions
which add valuable insights to the field. Instead, strong submissions tend to
leverage the authors code to make exhaustive ablations, hyperparameter search
and explore generalisability results on different data/models.

### Redundant reproductions of the same resource-friendly papers

For several years, we find that authors tend to pick papers which are more
resource-friendly - i.e. papers which can run on a single commodity GPU. This is
likely a side-effect of the challenge being targeted primarily towards early
career researchers. While reproducibility study on such resource-light papers is
not a problem per se, it does often result in multiple reproduction reports on
the same paper. We hypothesize that this is probably due to courses assigning
multiple groups to work on a single paper, in order to better manage logistics.
As we did not have any deduplication criteria, we explicitly inform our
reviewers to not penalize multiple reproducibility reports on the same paper. We
aimed to reduce this by introducing a pre-registration phase early on
([2019](https://www.cs.mcgill.ca/~jpineau/ICLR2019-ReproducibilityChallenge.html),
[2020](https://paperswithcode.com/rc2020/registration)), however that turned out
to be logistically challenging leading us to discontinue it. In our opinion,
cherry-picking the same paper reduces the breadth of papers being reproduced in
the challenge, invites duplication in work and overall lessens the scientific
contribution to the community.

### Low signal reviews due to inexperienced reviewers

Reviewing for the ML Reproducibility Challenge is unique - it requires the
reviewer to first read and understand the original paper(s) and then perform a
critical judgment of the reproducibility report. Hence, workload wise, reviewing
for this challenge requires twice the amount of time per paper than a standard
ML conference. We therefore typically try to evenly reduce the reviewing
workload, with a maximum of two papers per reviewer. Over the last several
iterations, barring from the top reviewers, we observed a concerning trend of
low signal reviews. We hypothesize this mainly due to the different format and
higher workload. To remedy this, we have introduced comprehensive reviewer
guidelines, and also awarded top reviewer awards to further incentivize high
quality reviews. We are grateful to our reviewers for their consistent support,
and we have observed a steady number of reviewers who consistently provide high
quality, useful reviews and hence feature in the top reviewers list on multiple
occasions.

### Low incentives to publish a reproducibility report

From the inception of the challenge, we have partnered with ReScience as our
journal publication medium. [ReScience](https://rescience.github.io/) is a peer
reviewed, open journal focusing on reproducibility reports across many different
fields of computational science, making it a unique venue. ReScience journal
editorial process is open and live on [Github](https://github.com/ReScience),
making it very convenient to access. However, we have observed that the
popularity of ReScience in the Machine Learning community is still low, limiting
the incentives of publication at the challenge. Furthermore, we found ReScience
journal entries are not yet
[properly indexed](https://github.com/ReScience/rescience.github.io/issues/113)
by Google Scholar, although the editors are working hard to fix that. Another
issue was since MLRC is not a workshop at any major conference, the original
format did not have any option to present papers to the community, hurting the
incentives even further. Since 2022, we have partnered with
[NeurIPS](https://blog.neurips.cc/2022/08/15/journal-showcase/) to allow poster
presentations of accepted papers at the Journal to Conference Track, which
significantly increases the incentive and prestige of publishing papers at MLRC.
We have also partnered with
[Kaggle](https://www.kaggle.com/reproducibility-challenge-2022) in our last
iteration to provide accepted papers compute credits to further incentivize
submission and high quality research. Authors of top papers were granted a
significant amount of compute credits by Kaggle to further pursue their
research.

## On the road ahead

We want to continue improving the challenge on the following aspects: broadening
the target audience, broadening the scope and improving incentives, to make the
challenge more exciting to the community and encourage reproducible research.

We are thus happy to announce the formal partnership with
[Transactions of Machine Learning Research (TMLR)](https://jmlr.org/tmlr/)
journal. TMLR is a new journal in the ML community, which is under the umbrella
of Journal of Machine Learning Research (JMLR), and has been fast growing in
significance and reputation within the field. Unlike JMLR, TMLR caters to
shorter format manuscripts similar to conference proceedings, and employs a fast
and open reviewing cycle, ensuring high quality submissions. Therefore, in the
upcoming iteration (MLRC 2023), papers will be published at TMLR instead of
ReScience.

### Broadening the target audience

While the MLRC will still be useful for the early-career researchers in ML
courses, we want to expand and encourage submissions from the broader community,
including academia and industry. Since TMLR publication accounts for
significantly high prestige and reception in the ML community, we hope this
change would attract a broad range of researchers to contribute to the
advancement of our understanding of reproducibility.

### Increasing the bar of submissions

As we look forward, the focus of a reproducibility paper should be much more
than mere reproduction - it should ideally investigate the generalisability of
the original claims. Results and investigations beyond what the authors proposed
are therefore encouraged, which adds to the novelty of the contribution. We
discourage simple replication work - while they are useful, they do not provide
enough value to the community. Submissions having multi-paper, topic-based
focused contributions are preferred over single paper reproductions. Novel work
on tools to investigate and enable reproducible research are also welcome to the
submission. We also recommend you to read TMLR’s
[submission guidelines and
editorial policies](https://jmlr.org/tmlr/editorial-policies.html) which also
applies equally to MLRC submissions.

### Implementing a comprehensive and open reviewing cycle

As we partner with TMLR, we also leverage their open, comprehensive reviewing
mechanism. Papers submitted to MLRC would first undergo TMLR’s reviewing
process. TMLR employs rich and diverse reviewers from the ML community, along
with expert Action Editors. Reviews will be viewed publicly on
[OpenReview](https://openreview.net/group?id=TMLR), and TMLR comes with a quick
reviewing turnaround which includes author rebuttals - a highly requested
feature in our previous iterations.

### Improving incentives to participate in the challenge

Publication of MLRC papers at TMLR will improve the reception and dissemination
of the work in the broader ML community. Accepted papers at TMLR are announced
in mailing lists and social media on
[a regular basis](https://jmlr.org/tmlr/contact.html). Papers accepted at TMLR
are indexed in Google Scholar using the existing OpenReview mechanism, allowing
easy citations and tracking cited counts. We also hope to continue our existing
partnership with NeurIPS to present accepted papers in the Journal to Conference
Showcase Track, allowing further dissemination and opportunity to gain feedback
from the ML community. (If you are attending NeurIPS 2023 in person, checkout
the Journal to Conference Track poster session for MLRC 2022 accepted papers!)

### Providing a new home for MLRC web

We are happy to announce our new and permanent online home,
[reproml.org](http://reproml.org). Announcements, information and blog posts
about MLRC 2023 and all subsequent iterations will be hosted in this dedicated
space. We are grateful to PapersWithCode for providing online hosting for our
past three iterations!

## MLRC 2023 Call for Papers

Finally, we are happy to formally announce MLRC 2023, which will go live
starting on **October 23rd**! We invite contributions from academics,
practitioners and industry researchers of the ML community to submit novel and
insightful reproducibility studies.

We recommend you choose any paper(s) published in the 2023 calendar year from
the top conferences and journals (NeurIPS, ICML, ICLR, ACL, EMNLP, ECCV, CVPR,
TMLR, JMLR, TACL) to run your reproducibility study on.

{{< figure src="../../uploads/mlrc.drawio.svg" class="mlrc_dark" >}}

{{< figure src="../../uploads/mlrc.light.drawio.svg" class="mlrc_light" >}}

In order for your paper to be submitted and presented at MLRC 2023, it first
needs to be **accepted and published** at TMLR. While TMLR aims to follow a
2-months timeline to complete the review process of its regular submissions,
this timeline is not guaranteed. If you haven’t already, we therefore recommend
submitting your original paper to TMLR by **February 16th, 2024**, that is a
little over 3 months in advance of the MLRC publication announcement date.

- Challenge goes live: October 23, 2023
- Deadline to share your intent to submit a TMLR paper to MLRC: February 16th,
  2024 **Form: https://forms.gle/JJ28rLwBSxMriyE89**. This form requires that
  you provide a link to your TMLR submission. Once it gets accepted (if it isn’t
  already), you should then update the same form with your paper camera ready
  details.
- Your accepted TMLR paper will finally undergo a light AC review to verify MLRC
  compatibility.
- We aim to announce the accepted papers by May 31st, 2024, pending decisions of
  all papers.

## Closing Thoughts

As we begin a new era of reproducibility research in Machine Learning, we hope
our continued quest for high quality reproducibility studies will inspire the
community to not only investigate the claims of existing papers, but add novel
research insights and contributions to the literature, accelerating the progress
of science. We hope these steps towards improving the incentives of investing in
reproducibility research enables the community to produce higher quality
scientific contributions.
