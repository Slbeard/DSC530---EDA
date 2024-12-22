# How Would the Death Data in Game of Thrones Be Altered if There Were No Magic?

This project explores how the death data in *Game of Thrones* would change if magical elements—such as dragons, White Walkers, and magical weapons—were removed. It analyzes the frequency and nature of deaths across seasons and episodes, investigating the effect of magic on who dies and how.

### Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy import stats
from scipy.stats import binom
import thinkstats2
import thinkplot
import random
import statsmodels.formula.api as smf
```
### Installation
```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels thinkstats2
```

### Data
The dataset game-of-thrones-deaths.xlsx contains the following columns:
- Name: Person who died.
- Allegiance: The house or group the deceased was aligned with.
- Season: Season in which the death occurred.
- Episode: Episode number in the season.
- Killer: Responsible party for the death.
- Killer's House: The house to which the killer belongs.
- Location: Location of the death.
- Method: The weapon used.
- Magical: Boolean indicating if magic was involved in the death (True/False).

### Magical Death Indicator
The Method column includes the following keywords to indicate if the death was magical:
- Dragon
- Demon
- Ice
- Magic
- Moon
- White Walker

### Key Updates
- Killer House Updates: The dataset was modified to properly categorize killers like "White Walker" and "Tribesman" under their respective houses.
- Magical Deaths: A new column was created to classify deaths based on whether the Method or Killer's House indicates magical involvement.
- Data Cleaning: Duplicates, such as individuals dying more than once, were flagged, and certain edge cases, such as "Dothraki Khal", were manually checked.

### Analysis
- Magical vs Non-Magical Deaths: Analyzed the total number of deaths with and without magical involvement.
- Seasonal and Episode Analysis: Visualized the distribution of deaths across seasons and episodes.
- Killer Analysis: Compared the most frequent killers with and without magical deaths.
- Weapon Analysis: Identified the most used weapons in non-magical deaths.
- Hypothesis Testing: Applied statistical tests to examine the significance of magical versus non-magical deaths.

### Visualizations
The project includes various plots such as:

- Seasonal death distribution (magical vs non-magical)
- Killers' frequency (overall and non-magical)
- Death frequency per episode and season
- Allegiance breakdown (with outliers removed)
- Regression analysis (for non-magical killers using magical methods)
