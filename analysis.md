#### quick analysis of the data from the terminal to have a first insight

# import pandas
```>>> import pandas as pd```

# load the species_info data
```>>> species = pd.read_csv("species_info.csv")```

# get an idea of the columns
```>>> print(species.head(5))
  category                scientific_name                                       common_names conservation_status
0   Mammal  Clethrionomys gapperi gapperi                           Gapper's Red-Backed Vole                 NaN
1   Mammal                      Bos bison                              American Bison, Bison                 NaN
2   Mammal                     Bos taurus  Aurochs, Aurochs, Domestic Cattle (Feral), Dom...                 NaN
3   Mammal                     Ovis aries  Domestic Sheep, Mouflon, Red Sheep, Sheep (Feral)                 NaN
4   Mammal                 Cervus elaphus                                      Wapiti Or Elk                 NaN```

# load the observations data
```>>> observations = pd.read_csv("observations.csv")```

# get an idea of the columns
```>>> print(observations.head(5))
            scientific_name                            park_name  observations
0        Vicia benghalensis  Great Smoky Mountains National Park            68
1            Neovison vison  Great Smoky Mountains National Park            77
2         Prunus subcordata               Yosemite National Park           138
3      Abutilon theophrasti                  Bryce National Park            84
4  Githopsis specularioides  Great Smoky Mountains National Park            85```

# describe the observations data for first statistic values
```>>> print(observations.describe())
       observations
count  23296.000000
mean     142.287904
std       69.890532
min        9.000000
25%       86.000000
50%      124.000000
75%      195.000000
max      321.000000```

# describe the species data for first statistic values
```>>> print(species.describe())
              category scientific_name        common_names conservation_status
count             5824            5824                5824                 191
unique               7            5541                5504                   4
top     Vascular Plant     Canis lupus  Brachythecium Moss  Species of Concern
freq              4470               3                   7                 161```

# check the types of the columns in species data
```>>> species.dtypes
category               object
scientific_name        object
common_names           object
conservation_status    object
dtype: object```

# check the types of columns in observations data
```>>> observations.dtypes
scientific_name    object
park_name          object
observations        int64
dtype: object```

# check if null values in species data
```>>> print(species.isnull().sum())
category                  0
scientific_name           0
common_names              0
conservation_status    5633
dtype: int64```

# check if null values in observations data
```>>> print(observations.isnull().sum())
scientific_name    0
park_name          0
observations       0
dtype: int64```

