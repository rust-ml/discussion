# Discussion
This repository/organization is the home of an informal Rust Machine Learning working group: think of it as a centralized discussion hub to make sure that efforts do not remain hidden and isolated in this early phase of the Rust Machine Learning ecosystem.

A space to discuss the future of the ML ecosystem in Rust, in the open.

The main discussion thread is [here](https://github.com/rust-ml/discussion/issues/1): please come and share your view!

# Work streams

We have identified different areas of focus:

- [**General-purpose pre-processing**](#general-purpose-pre-processing)
- [**NLP**](#nlp)
- [**Classical ML**](#classical-ml)
- [**Deep Learning**](#deep-learning)
- [**Deployment**](#deployment)
- [**DataFrames**](#dataframes)
- [**Interoperability**](#interoperability)
- [**Reinforcement Learning**](#reinforcement-learning)
- [**Computer Vision**](#computer-vision)

Every single one of these areas is looking for contributors!


## General-purpose pre-processing

A sufficiently complete toolkit to mold raw data before getting into a machine learning model (dimensionality reduction, scaling/normalisation, discretization, missing value imputation, etc.).

Contributors: [@jblondin](https://github.com/jblondin), [@LukeMathWalker](https://github.com/LukeMathWalker)

Repository: [nlp-discussion](https://github.com/rust-ml/classical-ml-discussion)

## NLP

Rust seems to have plenty of small crates, more or less experimental, for dealing with natural language (see also [this](https://users.rust-lang.org/t/interest-for-nlp-in-rust/15331) discussion on Rust internals). It's probably time to coordinate: identify functionality gaps, generalize some of the existing crates and create a coherent story.

Contributors: [@jbowles](https://github.com/jbowles), [@danieldk](https://github.com/danieldk), [@rth](https://github.com/rth), [@sebpuetz](https://github.com/sebpuetz)

Repository: [nlp-discussion](https://github.com/rust-ml/nlp-discussion)

## Classical ML

There are several unmaintained crates (e.g. [rustlearn](https://github.com/maciejkula/rustlearn), [rusty-machine](https://github.com/AtheMathmo/rusty-machine)). The language and the ecosystem have moved considerably forward since those experiments and now it's a good time to isolate core components and provide a set of community-backed interfaces for ML models and pipelines, making sure they are fit for purpose by trying them out while implementing or porting classical ML algorithms (trees, SVMs, Gaussian Processes, clustering, etc.). Some of these algorithms already exists, scattered in different crates, at different stages of maturity and maintenance - coordination and re-use should be promoted whenever possible.

Contributors: [@LukeMathWalker](https://github.com/LukeMathWalker)

Repository: [nlp-discussion](https://github.com/rust-ml/classical-ml-discussion)

## Deep Learning

There are bindings for both `PyTorch` ([tch-rs](https://github.com/LaurentMazare/tch-rs)) and `Tensorflow` ([tensorflow](https://github.com/tensorflow/rust)), but they could use some love to fill in the gaps and polish the API.

There is ongoing work in the [TVM](https://tvm.ai/) project: there are Rust bindings for the runtime, but no bindings to the TVM compiler. TVM could be used as backend for a high-level DL library in Rust, thus providing access to a wide range of different hardwares.

At the same time, there is interest in exploring the feasibility and ergonomics of a pure-Rust crate for DL.

## Deployment

Bridging the gap from a working prototype to production: Rust has a chance to shine here, putting to use well known crates such as [rocket](https://rocket.rs/). Getting a model exposed behind a performant API should be a matter of configuration: what protocol do I want to use (HTTP/gRPC/etc.), where is the model, do I want to expose Prometheus metrics, where do I send the logs. Done, shipped.

## DataFrames

There is an ongoing discussion [here](https://github.com/rust-dataframe/discussion/issues) on what challenges a DataFrame library in Rust should tackle and what design constraints it should obey.

## Interoperability

No ecosystem is an island: we need to be able to serialize and deserialize the most common file formats in the ML/data space - hdf5, Parquet, NumPy's npy, etc.
Each of these format has seen some work, but the maturity of the corresponding crate might vary.

## Reinforcement Learning

It has been mentioned that Rust could be used to develop training environments/gyms for RL models. Is there latitude to interact with the work of the Rust gamedev community?

## Computer Vision

[opencv-rust](https://github.com/twistedfall/opencv-rust) was mentioned, and @xd009642 is working on [ndarray-vision](https://github.com/xd009642/ndarray-vision). The topic was not extensively discussed, but there might be a wider community interested that we haven't been able to intercept here.

