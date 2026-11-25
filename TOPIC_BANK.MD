## 1. HealthForesight: model that predicts malnutrtion

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

## 2. Scholarship Finder
- **Idea:** A chatbot that reads official scholarship guidelines (DOST-SEI, CHED, LGU, and university scholarships) and tells a student which ones they may qualify for, citing the exact section and linking the official page. It accepts questions in English, Filipino, or Taglish.
- **Problem it addresses:** Scholarship information is scattered across many sites, each with its own requirements and deadlines. Students miss scholarships they qualify for.
- **Closest existing work:**
    - *Scholarship recommendation with ML:* an [IEEE Access (2024) blockchain scholarship platform](https://doaj.org/article/79054c39cb354384ac1d3e4e8448bf8f) uses a model to predict scholarship qualification (86.75% balanced accuracy); [Kanwal et al. (2024)](https://techscience.com/iasc/v39n5/58466/html) compare SVM, neural networks, KNN, and C4.5 for scholarship eligibility; [Bambi (2026)](https://www.mecs-press.org/ijitcs/ijitcs-v18-n3/IJITCS-V18-N3-4.pdf) uses ensemble learning to recommend awardees; [EduScholar AI](https://www.ijert.org/research/eduscholar-ai-ai-powered-scholarship-recommendation-system-IJERTV15IS070495.pdf) matches student profiles to scholarship schemes. Most of these help committees *select* students; ours helps students *find* scholarships, with citations to the official rules.
    - *Philippine student-support chatbots:* UPOU's [Ask Iska and IskOU (2021)](https://ijodel.upou.edu.ph/ijodel/article/view/45/130) answers student questions; UPOU's [advanced chatbot ecosystem project](https://fics.upou.edu.ph/news/upou-to-launch-four-year-project-on-advanced-chatbot-ecosystem-for-student-support/) is a four-year student-support initiative. Neither focuses on scholarship eligibility.
- **Data needed:** Public scholarship guidelines and announcements, saved as PDFs or web pages with their publication dates.
- **Compute needed:** Colab GPU for a small open model, or a hosted API.
- **Biggest risk:** A wrong "you don't qualify" answer could make a student skip a real chance. Guidelines also change every year.
- **Team interest:** _/5 · **Feasibility:** 4/5


## 3. Government spending anomaly finder
- **Idea:** Flag unusual government procurement contracts in PhilGEPS for human review: unit prices far above what other agencies paid for the same item, the same suppliers winning repeatedly, and purchases split into many small contracts just under the public-bidding threshold.
- **Problem it addresses:** Overpricing and rigged bids waste public funds. Audits find them late, usually after the money is spent, and no one can manually review every contract.
- **Closest existing work:** Procurement "red flag" indicators from corruption research, such as [Fazekas, Tóth, and King (2016)](https://doi.org/10.1007/s10610-016-9308-z), *An Objective Corruption Risk Index Using Public Procurement Data*. Confirm in the literature review whether anyone has applied them to PhilGEPS.
- **Data needed:** Bid notices and contract awards from the [PhilGEPS Open Data portal](https://philgeps.gov.ph/CmsHomePages/open-data); COA annual audit reports to check our flags against.
- **Compute needed:** Laptop; Python with pandas and scikit-learn (Isolation Forest, simple statistical outlier rules).
- **Biggest risk:** No answer key: there is no official list of "bad" contracts. PhilGEPS records are also incomplete, with missing prices or suppliers.
- **Team interest:** _/5 · **Feasibility:** 3/5
