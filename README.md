# OpenNeuro Derivatives

The OpenNeuro Derivatives Project is an effort to provide quality control
metrics and preprocessed data for all raw datasets on OpenNeuro.

This superdataset is an aggregation of derivative datasets produced by
running [BIDS Apps](https://bids-apps.neuroimaging.io/) on
raw datasets from [OpenNeuro](https://openneuro.org/).

## Contents

Derivatives currently included, grouped by the tool that produced them:

| Tool                                       | Description                                 |
| ------------------------------------------ | ------------------------------------------- |
| [MRIQC](https://mriqc.readthedocs.io/)     | Image quality metrics for T1w and BOLD      |
| [fMRIPrep](https://fmriprep.org/)          | Anatomical and functional MRI preprocessing |
| [FitLins](https://fitlins.readthedocs.io/) | Subject- and group-level GLM analyses       |
| [XCP-D](https://xcp-d.readthedocs.io/)     | Post-processing for resting-state fMRI      |

## Usage

The superdataset is intended to be cloned with [DataLad](https://www.datalad.org/):

```bash
datalad clone https://github.com/OpenNeuroDerivatives/OpenNeuroDerivatives.git
cd OpenNeuroDerivatives
datalad get ds000001-fmriprep         # install and download a full subdataset
datalad get ds000001-fmriprep/sub-01  # fetch one subject's files
```

Each subdataset has its own `README.md` describing the tool version, the
methods boilerplate (where applicable), the compute environment, and the
source OpenNeuro dataset.

## Methods

See each subdataset's `README.md`, `dataset_description.json`, and `code/` directory
for details on the methods used to generate the derivatives.

## Citing

Most subdatasets do not have independent DOIs.
To cite them, please cite the source OpenNeuro dataset,
this superdataset, and the BIDS App that produced the derivatives.
Please also consult each subdataset's README and `dataset_description.json`
for any additional citation instructions.

To cite this aggregation, see [`CITATION.cff`](./CITATION.cff).

## Acknowledgements

This work was funded by the NIH BRAIN Initiative under award
[R24-MH117179](https://reporter.nih.gov/project-details/11128603) to
Russell A. Poldrack.

Computing for the MRIQC, fMRIPrep, and XCP-D derivatives was performed on
the TACC Frontera system under the Pathways allocation.
We thank TACC for providing computational resources and support.
Please cite Frontera as:

> Dan Stanzione, John West, R. Todd Evans, Tommy Minyard, Omar Ghattas, and
> Dhabaleswar K. Panda. 2020. Frontera: The Evolution of Leadership Computing
> at the National Science Foundation. In _Practice and Experience in Advanced
> Research Computing_ (PEARC '20), July 26–30, 2020, Portland, OR, USA. ACM,
> New York, NY, USA, 11 pages.
> <https://doi.org/10.1145/3311790.3396656>

Computing for the FitLins derivatives was performed on the Sherlock cluster.
We would like to thank Stanford University and the Stanford Research Computing Center
for providing computational resources and support
that contributed to these research results.

## License

Released under [CC0 1.0 Universal](./LICENSE).
Subdatasets are also CC0 unless otherwise indicated.

### Disclaimer

These data are provided on an "as is" basis, and no warranties are expressed or implied
pertaining to the quality of the data, or any specific purpose of use.
Data consumers are responsible for evaluating
the quality of the derivatives for their intended uses.
