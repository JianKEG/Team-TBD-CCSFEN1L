1. HealthForesight: model that predicts malnutrtion

- **Idea:** Estimate each province's child malnutrition rate (stunting, underweight,
wasting) from public data, then show the estimates on a map.
- **Problem it addresses:** National nutrition surveys are expensive and run only every
few years. Between surveys, nutrition offices and DepEd divisions plan feeding
programs with outdated numbers.
- **Closest existing work:** Siy Van et al. (2022) predicted undernutrition for 618 individual
Filipino schoolchildren from household surveys; Ong Yiu et al. (2024) improved on it
with the same data. Jean et al. (2016) estimated poverty from satellite images and
machine learning.
- **Data needed:** Malnutrition
rate from public data such as poverty statistics and satellite night-lights.
- **Compute needed:** Laptop; Python with pandas, scikit-learn, and geopandas for the
map.
- **Biggest risk:** Provincial rates for ages 5 to 10 may not be published. If only under-5
rates exist (OPT+), the thesis switches to early-childhood malnutrition. With about 80
provinces, the dataset is also small.
- **Team interest:** 5/5 · **Feasibility:** 4/5
