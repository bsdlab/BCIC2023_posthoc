# Post-Hoc Relabeling

### Basic idea

This is use case example of the _Post-Hoc relabeling_ method developed by Castaño-Candamil et al., 2019, in [Post-hoc Labeling of Arbitrary M/EEG Recordings for Data-Efficient Evaluation of Neural Decoding Methods](https://www.frontiersin.org/articles/10.3389/fninf.2019.00055/full). The basic idea as detailed in the paper, builds on the assumption cognitive and motor activity can be decoded from narrow band power of just a few bipol sources. The method uses existing arbitray EEG/MEG recordings and derives source space activity from them. This can be done following either:

1. An anatomically constrained mode, where a forward model, e.g. derived from an average head, is used to estimate the sources activity;
1. data driven approach, which uses any blind source separation method, such as e.g. ICA, to derive synthetic sources.
   With these source projections, the user can manipulate source data to synthetically create certain features like signal power or SNR.

### This notebook

This notebook will demonstrate the use of the _Post-Hoc Relabeling_ method to generate augmented EEG for evaluating the impact of regularization following the extended CSP approach (rCSP) proposed by [Lotte et al., 2010](https://ieeexplore.ieee.org/document/5593210). We will make use of the data driven approach by extracting ICA sources from a single subjects session of the [`Schirrmeister2017`](http://moabb.neurotechx.com/docs/generated/moabb.datasets.Schirrmeister2017.html) [MOABB](http://moabb.neurotechx.com/docs/index.html) data set.
