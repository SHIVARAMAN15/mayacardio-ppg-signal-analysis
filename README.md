# MayaCardio PPG Signal Analysis

## Objective
Analyze five PPG recordings to examine signal quality, packet integrity, frequency content, and the effect of an exploratory filtering method.

## Tools
- Python
- NumPy and Pandas
- SciPy
- Matplotlib
- Google Colab / Jupyter Notebook

## Analysis
1. Reconstruct recordings from packets and inspect sequence numbers and sample indices.
2. Plot all five unmodified PPG recordings.
3. Compare S1 and S3 in the time and frequency domains.
4. Apply an exploratory 8 Hz low-pass Butterworth filter to S3.
5. Compare detected peaks and their timing before and after filtering.
6. Discuss sampling, aliasing, filtering trade-offs, and possible fault locations.

## Main observations
- S5 has missing packets 20 and 21, corresponding to a one-second gap from 10 to 11 seconds.
- S3 has substantially greater high-frequency variation than S1.
- The exploratory filter reduces rapid variation, but changes in pulse morphology and an unmatched event require further review.

## Limitations
The physical source of the high-frequency component is not confirmed. The filtering method is exploratory and is not clinically validated. Peak-detection results depend on the selected parameters and require further testing.

## Reproducibility
Open `notebooks/MayaCardio_PPG_Analysis.ipynb` and run the cells in order. Place the supplied dataset in the expected working directory before running the notebook.

## AI-use disclosure
ChatGPT assisted with analysis planning, code drafting and debugging, and interpretation of results. Code outputs were reviewed in Google Colab. Conclusions about the physical source of the observed variation remain uncertain.
