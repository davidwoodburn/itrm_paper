---
title: 'itrm: Interactive Terminal Utilities'
tags:
  - Python
  - plotting
  - analysis
  - interactive
authors:
  - name: David Woodburn
    orcid: 0009-0000-5935-2850
    equal-contrib: false
    affiliation: 1
affiliations:
 - name: Air Force Institute of Technology, USA
   index: 1
date: 02 October 2024
bibliography: paper.bib
---

# Summary

Many developers, engineers, and scientists spend significant time working within
terminal environments, where switching contexts to generate visual plots can be
both time-consuming and annoying. Traditional plotting tools, while effective
for producing polished final figures, are often insufficient for quickly
inspecting and understanding data. Curious to see what the frequency content of
the data is? Want to filter out the high-frequency noise so you can see a
pattern more clearly? Interested in the derivative of the data? All these will
typically require you go back to your source and write several lines of code
before you can see the results. This challenge is amplified when working
remotely with a server, where visualizing data often requires saving it to a
file, transferring it to a local machine, and writing scripts to generate
plots—a tedious and repetitive process. A more efficient solution is needed to
streamline data visualization and interaction directly within the terminal.

The `itrm` [@itrm] library provides the only known, terminal-based solution for
interactively analyzing data. It is written in pure Python and aside from some
builtin modules has only NumPy as a dependency.

# Statement of need

There are already several terminal-based plotting tools available, several of
them written for Python. The following table summarizes a non-exhaustive list
these tools:

| Name  | Author | Language | Line plots  | Y-axis | Resolution |
| ----- | ------ | -------- | ----------- | ------ | ---------- |
| `asciichartpy` | @asciichartpy | Python | yes | yes     | low  |
| `bashplotlib`  | @bashplotlib  | Python | yes | no      | low  |
| `drawille`     | @drawille     | Python | no  | no      | high |
| `pipeplot`     | @pipeplot     | Python | no  | no      | low  |
| `plotext`      | @plotext      | Python | yes | limited | high |
| `plotille`     | @plotille     | Python | yes | limited | high |
| `pysparklines` | @pysparklines | Python | no  | no      | high |
| `termgraph`    | @termgraph    | Python | no  | yes     | high |
| `terminalplot` | @terminalplot | Python | yes | no      | low  |
| `termplot`     | @termplot     | Python | no  | no      | low  |
| `termplotlib`  | @termplotlib  | Python | yes | limited | low  |
| `uniplot`      | @uniplot      | Python | yes | limited | half |
| `gnuplot`      | @gnuplot      | C      | yes | limited | low  |
| `termeter`     | @termeter     | Go     | yes | limited | high |
| `ttyplot`      | @ttyplot      | C      | no  | limited | low  |
| `youplot`      | @youplot      | Ruby   | yes | limited | high |

None of these tools is interactive in the sense of providing data point
inspection, view zooming and panning, point-to-point comparisons, etc. And,
certainly none of them provide the ability to process the data with common
transforms on the fly. Only a few of them provide sub-character resolution
through the use of Braille characters.

The `itrm` package has been downloaded about [35k
times](https://www.pepy.tech/projects/itrm). It is currently the author's
work-horse data analysis tool for his research at the Air Force Institute of
Technology in inertial navigation, Bayesian estimation, and space-weather
anomalies.

# References
