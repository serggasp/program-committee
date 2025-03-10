## dblp

- [website](https://dblp.org/) and [mirror 1](https://dblp.uni-trier.de/)
- [blog post about DBLP SPARQL service](https://blog.dblp.org/2024/09/09/introducing-our-public-sparql-query-service/)

## examples of conferences

### SOFSEM

- [website](http://www.sofsem.sk/) including a list of topics
- [dblp entry](https://dblp.org/db/conf/sofsem/index.html)

### FOCS

- [website](https://ieee-focs.org/)
- [2025 website](https://focs.computer.org/2025/) including a list of topics in the Call for Papers
- [dblp entry](https://dblp.org/db/conf/focs/index.html)

## input provided by user

- acronym of conference (possibly by selecting the DBLP stream name from a list)
- size of program committee
- expected number of submissions
- number of PC members assigned to review each paper [default: 3]
- list of topics

## data challenges

- given a list of topics and a list of researchers, determine how strongly each researcher covers each topic from publicly available data
- for each researcher, determine the country/countries of their host institution(s)
- for each researcher, determine their seniority (a proxy is the number of years since their first published paper) and gender

## typical workflow for creating a PC

1. the steering committee of the conference selects 1-3 chairs of the PC
2. then, the PC chairs define the topics of the conference (usually same as previous year, with minor modifications), estimate the number of submissions, and set the number of reviews per paper
3. then, the PC chairs form the program committee (this project helps doing exactly this step)
4. then, authors are invited to submit papers to the conference via a call-for-papers and the submission system opens
5. then, papers are submitted to the conference,
6. after the paper submission deadline, PC members express their preferences for which papers they would like to review
7. then, PC chairs assign each paper to the number of PC members defined in step 2

In particular, this means that this software does not know the topics of the submitted papers, but this can can be estimated based on data from previous years.

We can assume that the PC chairs have a list of topics (and a draft call for papers) that they can provide to this software.

In general, the expertise of the PC should match the expected submissions. In particular, for unpopular topics where we only expect 1-2 submissions, we do not necessarily need 3 PC members who are familiar with this topic, since a PC member who is assigned to an unfamiliar paper is typically allowed to outsource the review to an external reviewer. Therefore, this system can ignore the input "number of PC members assigned to review each paper [default: 3]" while selecting candidates for the PC. This input could be used to prepare an invitation email though, where we inform the potential PC member of their workload, such as: 
> each PC member is expected to be assigned 15-20 papers and we expect you outsource at most 50% of your reviews to external reviewers.

## target conferences

The relevant conferences are computer science conferences with a flat PC. This is where the PC consists only of PC chairs and PC members, without any further hierarchy.

Note: The system could be the basis for a variant of the system for hierarchical PC as well, where the PC chairs use the system to identify area chairs, each area chair uses the system to select senior PC members, and then senior PC members select regular PC members.
