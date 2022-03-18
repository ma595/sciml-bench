<img src="./sciml_bench/docs/resources/logo.png" alt="logo" width="500"/>



# SciML-Bench: Table of Contents
- [1. Synopsis](#1-synopsis)
- [2. Benchmark Suite](#2-benchmark-suite)
  * [2.1 Organisation](#21-organisation)
  * [2.2 Features](#22-features)
  * [2.3 Benchmarks and Datasets](#23-benchmarks-and-datasets)
- [3. Installation and Usage](#3-installation-and-usage)
- [4. Citation](#4-citation)
- [5. Acknowledgments](#5-acknowledgments)



# 1. Synopsis

Benchmarking is a valuable tool in computational science that allows effective comparison of software and/or hardware systems.  With the rise of machine learning and AI, the need for benchmarking AI algorithms is  increasing. The SciMLBench is aimed at the ‘*AI for Science*’ research community.  

With an ever-growing number of machine learning models and algorithms, a range of scientific problems, and the proliferation of AI systems, the development of cutting-edge ML/AI algorithms requires a detailed understanding of all of these aspects as well as effective mechanisms for measuring their effectiveness.

The SciML-Bench toolkit aims to provide such mechanisms. It is an open-source initiative and covers a range of scientific problems from various domains of science, including materials, life and environmental scienceS, as well as particle physics and astronomy. The benchmarks are implemented in Python and rely on one or more machine learning frameworks, such as TensorFlow, PyTorch or SciKit-Learn.

The overarching purpose of this initiative is to support the ‘*AI for Science*’ community in the development of more powerful, robust and understandable machine learning solutions.


# 2. Benchmark Suite 


## 2.1 Organisation

The suite has three components, namely, 

1. **Benchmarks**: In our case, a benchmark is a machine learning application performing a specific scientific task, written in Python. These are included as part of the distribution, and can be found inside the ``./sciml_bench/benchmarks`` directory. In the scale of *micro-apps*, *mini-apps*, and *apps*, benchmarks are full-fledged applications. 

2. **Datasets**: Each benchmark in (1) relies on one or more datasets, for example for training and/or inference. These datasets are open, task- or domain-specific, and FAIR compliant. Most of these datasets being large, they are hosted separately,  on one of the servers (or mirrors), and are downloaded separately on demand. The framework (see (3)), supports manual downloading of these datasets. 

3. **Framework**:  The framework serves two purposes: first, at the user level, it facilitates an easier approach to benchmarking, logging and reporting of the results. Secondly, at the developer level, it provides a coherent API for unifying and simplifying the development of AI benchmarks. Sources related to the framework can be found inside the ``./sciml_bench/core`` directory. 

The source tree, which captures these aspects,  is organised as follows:

```bash
├── README.md                   <This file>
└── sciml_bench/                <Root folder for the framework and benchmarks>
    ├── core/                   <Core scripts> 
    └── docs/                   <Main documentation folder>
        ├── full/               <Full HTML documentation> 
        ├── benchmarks/         <Documentation on benchmarks>
        ├── datasets/           <Documentation on datasets>
        ├── resources/          <image and other resources for documentation> 
    ├── benchmarks/             <Benchmark sources> 
    |   └──.../                 <Various benchmarks>
    └── etc/                    <Extra core files>
        ├── configs/            <Configuration files> 
        ├── recipes/            <Container and other recipes>
        └── templates/          <Template files> 

```

We have annotated the purpose of each folder/directory within `<>`.  

## 2.2 Features 

A typical user-base for the benchmarking framework may cover a broad spectrum of user communities, such as system manufacturers and integrators (for assessing system performance), scientists (for developing new algorithms), and computer scientists  or ML enthusiasts (for understanding the basics of various machine learning models and algorithms). It is a challenging task to design for and cover all these requirements in a single framework. Here, with SciML-Bench, we have attempted to cover these requirements through the following set of features:

* Very flexible, customisable and lightweight framework,
* Powerful logging and monitoring capabilities, 
* Support for multiple machine learning frameworks (TensorFlow, PyTorch, Apache MXNet, and SciKit-Learn), 
* Simplified application programming interface (API), to support easier development of benchmarks, 
* Fully customisable installation, 
* Simplified use of framework that encourages a wide range of users, and
* Fully decoupled, on-demand, and user-initiated data downloads. 



## 2.3 Benchmarks and Datasets 
The number of datasets and benchmarks may vary with every release. Please consult the [Benchmarks](./sciml_bench/docs/full/benchmarks/summary.html) and  [Datasets](./sciml_bench/docs/full/datasets/summary.html) documents for more details. You can also check out the full documentation [here](./sciml_bench/docs/full/index.html). A number of authors have contributed towards the development of the benchmarks,  and these contributions are stated in [Credits](./sciml_bench/docs/full/credits.html). If you are thinking of contributing towards the benchmarks or datasets, please see the [Contributing Datasets & Benchmarks](./sciml_bench/docs/full/main/contributing.html).



# 3. Installation and Usage

Please consult  [Installation & Usage](./sciml_bench/docs/full/main/usage.html) for getting started. The [Frequently Asked Questions (FAQ)](./sciml_bench/docs/full/main/faq.html) covers a number of installation issues. We have also included a short [tutorial]((./sciml_bench/docs/full/main/tutorial.html)) on installing and using the framework. 



# 4. Citation 

Cite this benchmark suite as follows:

    ```
    @misc{scimlbench:2021,
        title  = {SciML-Bench: A Benchmarking Suite for AI for Science},
        author = {Jeyan Thiyagalingam, Juri Papay, Kuangdai Leng, Samuel Jackson, Mallikarjun Shankar, Geoffrey Fox,  Tony Hey},
        url    = {https://github.com/stfc-sciml/sciml-bench},
        year   = {2021}
    }
    ```


# 5. Acknowledgments

This benchmarking programme is supported by [1] Wave I of the UKRI Strategic Priorities Fund under the EPSRC grant (EP/T001569/1), particularly the *AI for Science* theme in that grant and the Alan Turing Institute, and [2] the Benchmarking for AI for Science at Exascale (BASE), EPSRC ExCALIBUR Phase I grant (EP/V001310/1). 

<div style="text-align: right">◼︎</div>

