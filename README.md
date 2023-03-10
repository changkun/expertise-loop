# Expertise in the Loop Considered Harmful?

![](./assets/teaser.jpg)

**The Impact of Expertise in the Loop for Exploring Machine Rationality** <br/>
**[Changkun Ou](https://changkun.de)**, **[Sven Mayer](https://sven-mayer.com)**, and **[Andreas Butz](http://butz.org)** <br/>
In 28th International Conference on Intelligent User Interfaces (IUI '23), March 27-31, 2023, Sydney, NSW, Australia. ACM, New York, NY, USA, 15 pages. <br/>
[https://doi.org/10.1145/3581641.3584040](https://doi.org/10.1145/3581641.3584040)

This repository includes the collected dataset (anonymized), and the source code of scripts to reproduce the results reported in the paper.

## Full Paper

The paper is available at [ou2023expertise.pdf](./ou2023expertise.pdf).

## Dataset

The dataset is collected from the developed system of the research project.
The [raw](./data/raw) folder contains the raw data collected from the developed system.
The [processed](./data/processed) folder contains pre-computed data frames for further
statistical analysis. See [data/README.md](./data/README.md) for more information.

## Scripts and Figures

The Python and R notebooks that reproduce the reported results in Section 4
can be found in the [notebooks](./notebooks) and [assets](./assets) folder.

## System

The system is developed in Go and consists of three frontend applications and one backend server.
For more information, see [system/README.md](./system/README.md).

## Contribute

The easiest way to contribute is to provide feedback! We would love to hear what you think. Please write to [research@changkun.de](mailto:research[at]changkun.de) for closer communication.

## Licenses and Citation

Copyright &copy; 2023. [LMU Munich Media Informatics Group](https://www.medien.ifi.lmu.de). All rights reserved.

The [dataset](./data) itself (i.e., metadata, generated files, generated optimizer configurations, etc), available in [Creative Commons Public Domain Dedication (CC-0)](https://creativecommons.org/share-your-work/public-domain/cc0/), represented the results from consented anonymous participants and was collected by [Changkun Ou](https://changkun.de). The contained "source code" (i.e., Go, Python, R, JavaScript, etc) of this work is made available under the terms of [GNU GPLv3](./LICENSE) (by default).

If you find our research helpful, we would appreciate a citation via:

```bibtex
@inproceedings{ou2023expertise,
	title        = {The Impact of Expertise in the Loop for Exploring Machine Rationality},
	author       = {Ou, Changkun and Mayer, Sven and Butz, Andreas},
	year         = 2023,
	booktitle    = {Proceedings of the 28th International Conference on Intelligent User Interfaces},
	location     = {Sydney, Australia},
	publisher    = {Association for Computing Machinery},
	address      = {New York, NY, USA},
	series       = {IUI '23},
	numpages     = 15,
	keywords     = {human-in-the-loop machine learning, adaptive human-computer interaction, rationality},
	doi          = {10.1145/3581641.3584040}
}
```