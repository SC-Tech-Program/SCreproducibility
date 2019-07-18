# Reproducibility Challenge

The Reproducibility Challenge Track was introduced in SC19 to manage the process of selecting a paper and working with its authors to develop a benchmark for the Student Cluster Competition (SCC).
Because the committee selects a paper accepted at the _previous_ conference, it begins its work months before that previous conference, i.e., more than a year before the conference it is serving. 
It holds in-person interviews with candidate author teams at the _previous_ conference.

## Paper selection process

The Reproducibility Challenge committee selects a paper accepted at the _previous_ conference to be the source of the benchmark for the SCC. **The SC19 committee selected a paper from SC18 as described here.**

Following the acceptance of SC18 papers, but still a few months before that conference, the Reproducibility Challenge chairs  requested access in Linklings to all of the papers that were submitted with an artifact appendix. 
For SC18, this was a list of 40 papers.  
In the first round of reviews, the committee evaluates feasibility for the competition. Ideally this first cut is done by September 1 and eliminates about 75% of the papers. For SC18, the 40 papers were cut down to 9. One reviewer per paper is sufficient.

A second round of reviews on the remaining papers targeted an October 1 deadline. Now, each paper should have at least three reviewers who look for which application is ideal for the SCC, not just feasibility. Following the review scores posted internally to the committee, a committee call was held to select the author teams to interview at SC18. The top-three author teams were contacted to request an interview at SC18, to inform them about the Reproducibility Challenge and to assess whether the application and author team will be a good fit for the Reproducibility Challenge in SC19. Some preference is given to applications with a concrete, real-world impact that will resonate with the students. 

For SC18, the three papers chosen were: 

- “Computing Planetary Interior Normal Modes with A Highly Parallel Polynomial Filtering Eigensolver”
- “Exploring Flexible Communications for Streamlining DNN Ensemble Training Pipelines”
- “Extreme Scale De Novo Metagenome Assembly”

At SC18, as many as possible of the SC19 Reproducibility Challenge team met with the short-listed authors in three separate meetings. The questions asked (see below) focused on the actual feasibility of adapting the application to the cluster competition in the cases where the information was not readily available in the submitted paper. In the case of SC18, all the applications appeared to be feasible, but one required UPC and GasNet, which may be more challenge than students are up for. Another was based around DNNs and may not work on a system with a non-NVIDIA accelerator.

Following the interviews the Reproducibility Challenge team meets and discusses to determine which application to invite. The invitation should be sent out in late December or early January.

### Interview questions for potential reproducibility application

**Questions for the author team**

- What platforms and architectures can this application run on?
- Do you expect similar or identical results on a different hardware architecture? 
- How much data does the application require for input? How much data does it produce?
- Can you produce multiple (at least 2) scaled down data sets to run on student clusters?
- Can the application be scaled to run on a modest-sized cluster?
- Can your team commit the time to working with the SCC team and the Reproducibility team to refactor your application/dataset and work with the student teams to get the code working?

**Questions for the Reproducibility team to consider**

- We need to gauge the author team’s excitement, interest, and whether they’ll be able to devote the time
- Does the application lend itself to a science story that can excite both the student teams and the public? Bonus points if it aligns with an SC theme or local/regional tie-in

## For future SC conferences

Since SC19, the AD Appendix is mandatory, which means that using the availability of an appendix for the paper pool to select a benchmark is no longer a filter.
Instead of starting with 40 papers, the SC20 team has the whole set of accepted papers (possibly around 100).

> We suggest that the SC20 team could start with the sub-set of papers that were found eligible for an Artifacts Available badge, a count of 32 accepted papers for SC19. This measure also has the effect of promoting a higher standard of reproducibility for future conferences.