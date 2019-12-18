# Reproducibility Challenge Digital Artifact at SC19

For the SCC 19 reproducibility challenge student teams were required to submit a digital artifact containing the results of their experiments. The following description was given to the students to structure their submissions.

## SCC19 Reproducibility Challenge Digital Artifact

Your team is taking on the challenge of reviewing an article for reproducibility entitled:  Computing Planetary Interior Normal Modes with A Highly Parallel Polynomial Filtering Eigensolver, which will be referred to as the “NormalModes” paper.

Reproducibility is one of the hallmarks of the scientific method. After three years of increasing momentum, the SC Reproducibility Initiative makes Artifact Description (AD) Appendices mandatory for all papers submitted to the SC19 Technical Program, but optional for workshop papers and posters. The SC Conference Series is committed to introducing activities that highlight, enhance, and reward participant efforts to improve reproducibility. We define an “artifact” to be a digital object that was either created by the authors to be used as part of the study or created by the experiment itself.

Your team will be required to submit a digital artifact for evaluation that will provide details into the steps your team took to review the article and to create a version of figure 7 figures for strong scaling and tables VI and VII in the Normal Modes paper, as well as any additional visualization of the normal modes for the given input planetary models.

While it is not required to use the exact styling and color schemes that are used in the Normal Modes paper and while it will not be factored in the review, you are encouraged to use a similar styling (type of chart, coloring, etc.) for the figures you will submit. Having similar stylings in the figures will aid the reviewers in making direct comparisons of your results with the ones presented in the Normal modes paper. This document will provide guidelines for how to package the artifact your team will submit.

The reproducibility challenge has to run on your competition cluster.

### Outline of the Digital Artifact

Your digital artifact should be packaged as a tarball or zipfile that will have a single directory and several subdirectories (detailed below). Populate the subdirectories with the necessary scripts, data, figures and tables created during the competition along with a description of what is contained in the artifact and instructions of how to run the code provided. The artifact will contain your reproducibility report and must be turned in before the end of the competition.

The digital artifact should contain:
.
└── ReproducibilityChallenge
    ├── compile
    ├── doc
    ├── figures
    │   ├── output
    │   └── scripts
    ├── input
    └── run
        ├── output
        └── scripts

#### The doc directory

The doc directory should contain a README. This can be in Markdown or plain text. This will serve as a guide to understand what the contents of the artifact are and how to use them. It should include:
* A description of the contents of the artifact
* Instructions on how to run/view/use each part of the artifact
* How to compare the artifact’s output with the output presented in the Normal Modes paper
The doc directory should also contain your final reproducibility report in .pdf format

#### The compile directory

* The compile directory should contain a “compilation” script or set of scripts. These scripts should produce the binaries and any other libraries used by the next “run” script(s). The scripts should build all major dependencies that are required by your build of the Normal Modes application. The output of this script should be the binaries used in the Normal Modes paper.
* Include a README in the compile directory that gives a brief explanation of how the script(s) work, including:
..* compiler information
..* Which software dependencies are being built by the script vs. supplied by the OS or .rpms
..* Any comments on what changes or modifications were done in order to compile on your cluster
* Include in the main README in the doc directory how to compile the application (i.e. how to invoke the script(s))
* In a separate file include the output from a script to gather system information.  Use https://github.com/SC-Tech-Program/Author-Kit (or a similar script) with appropriate modifications.

#### The run directory

The run directory should contain two subdirectories a scripts subdirectory and an output subdirectory.

##### scripts subdirectory

The scripts subdirectory should contain a “run” script. This script actually runs the application for the given planetary models input and creates the logs/output (in this case the normal modes of the planetary models) and results used in the “figures” script. The README should describe how the “run” script is used including:
* options and environment variables, etc.
* Environment at run time (e.g. env output)
* how runs resulting from the script differ from the experimental runs in the Normal modes paper (e.g. input data sets, number of processes, etc.)
* Indicate how timings were measured

##### output subdirectory

The output subdirectory should contain logs/output resulting from the “run” script. These result files are those used by the “figures” script. You could, for example, use the output subdirectory as the target for the output of your run scripts in the run/scripts subdirectory.

#### The figures directory

The figures directory should contain two subdirectories a scripts subdirectory and an output subdirectory.

##### scripts subdirectory

The script subdirectory should contain a “figures” script. This script takes the logs and output from running the “run” script in order to create your cluster’s version of figures 7 and strong scaling graphs for table VII with your cluster included, and tables VI and VII in the Normal Modes paper, as well as the .vtk visualizations of the normal modes for the given input planetary models and specified modes. The README should detail how the “figures” script is run, and what tools and software were utilized.

##### output subdirectory
The figures/output directory should contain tables, charts and figures that result from running the “figures” script. The README should include:
* a brief description of the results seen in the output plots (this commentary can be largely taken from the report text)
* comment the speedups/performance on the team’s machine and compare them the results in the Normal Modes paper (this can also largely be taken from the report text)

### Tools to prepare your submission

Your team may write your scripts in a shell scripting language or Python. If you feel you need to use another scripting language please check with the competition organizers. You can also optionally use automation tools to help you prepare your submission. If you do use one of these make sure to document your settings and turn them in with your report and artifact. Feel free to try them and give us your feedback:
* Spack: a flexible package manager that supports multiple versions, configurations, platforms, and compilers
* EasyBuild: software build and installation framework to manage scientific software on HPC systems in an efficient way
* CK: Guide to help you create, run and pack your SCC workflow
* Popper: Guide on creating a workflow from an existing set of scripts
