# Central Data

## These are just some data files I use a lot, and could maybe be useful to other people. Here's a quick description:

**GOSE_TTV_summaryfile.csv** -- This is a one-stop shop for transit timings. I've taken 500 draws from the joint posteriors produced for our Orbital Sampling Effect paper ([Paper](https://ui.adsabs.harvard.edu/abs/2018AJ....155...36T/abstract) | [Repository](https://github.com/alexteachey/TTV_posteriors)) to produce transit timings and uncertainties (see the paper for more information on the methodology). From there I just fit a line to get a best period linear ephemeris, and computed deviations from that line. Fast and dirty. *This is a comma-separated value file... open with Excel (or alternative) or Pandas.*

**cumkoi_forecast_masses.csv** -- Takes the planet radii for every KOI in the cumulative KOI list from NASA Exoplanet Archive (as of January 28, 2021) and uses the [FORECASTER code](https://github.com/chenjj2/forecaster) to predict masses for these planets. Note that this has been done in a far more sophisticated manner by Chen and Kipping ([Paper](https://ui.adsabs.harvard.edu/abs/2018MNRAS.473.2753C/abstract) | [Repository](https://github.com/chenjj2/forecasts)) but this is maybe a bit easier to access. *This is a comma-separated value file... open with Excel (or alternative) or Pandas.*

**every_kic_lc_list.npy** -- Prett self-explanatory. It should be a list of every KIC light curve. Note this is *NOT* the same thing as the full list of KICs... there's a whole lot more of those (about 13 million?). This is the list of the ~200,000 light curves that were obtained by *Kepler* -- many of which do not have known planets, but are downloadable. *This is a numpy array. Load using numpy.load()*

**every_kic_lc_without_a_planet.npy** -- Sometimes you want to look at a light curve that isn't ruined by all those pesky planets. This list is for you. *This is a numpy array. Load using numpy.load() *
