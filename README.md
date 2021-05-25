# Biostats data sets

___


### [data/mushroom_growth.csv](https://raw.githubusercontent.com/gzahn/biostats_data/main/data/mushroom_growth.csv)

#### Data set measuring effect of various growth conditions on two species of culinary mushrooms

<br>

##### Main question(s): 

-	What combination of factors yields the fastest growth?

-	Which factors are significant predictors of increased growth?

<br>

Variables:

+ **Species**		Mushroom species - Categorical

+ **Light**		Amount of light (hr/day) - 0, 10, 20

+ **Nitrogen**	Amount of nitrogen in substrate (g N / kg substrate) - 0,5,10,15,20,25,30,40,45

+ **Humidity**	Humidity condition - Ordered category - (high, low)

+ **Temperature**	Growth temperature (deg C) - Continuous - 20,25

+ **GrowthRate**	Response - Continuous - Mushroom mass increase - (g/day)

<br>


[Visualization](https://raw.githubusercontent.com/gzahn/biostats_data/main/figs/mush_groth.png)

___


### [data/microbial_carbon_metabolism.csv](https://raw.githubusercontent.com/gzahn/biostats_data/main/data/microbial_carbon_metabolism.csv)

#### Data set measuring carbon utilization potential of natural microbial communities. Samples from 4 sites were taken and added to "BioLog" plates at various dilutions. 

#### Each biolog plate has wells with 32 carbon-containing molecules. If that carbon source is utilized by the microbes, the color of the well changes.

#### UV light absorbance measures the relative amount of carbon utilization by the microbes in a given sample.

#### Water is the negative control and all other absorbance values have been normalized to the water samples.

<br>

##### Main question(s):

-	How does time affect carbon utilization in water vs soil?

-	Which communities (soil vs water) are able to use more diverse carbon sources (i.e., which has more biochemical pathways present)?

<br>

Variables:

+ **Site**		Sampling location - Categorical - Clear_Creek, Waste_Water, Soil_1, Soil_2

+ **Sample_Type**	Categorical - Water, Soil

+ **Rep**		Experimental replicate - Categorical - 1, 2, 3

+ **Dilution**	Sample dilution factor - Ordered category - 0.001, 0.010, 0.100

+ **Substrate**	Carbon source - Categorical - long list of carbon sources

+ **Time**		Hours since inoculation - Continuous - 24, 48, 144

+ **Absorbance**	Response - Proxy for carbon utilization (amount of UV light absorbance) - Continuous - no unit

<br>

[Visualization](https://raw.githubusercontent.com/gzahn/biostats_data/main/figs/C-utilization.png)

___

### [data/dwarf_bear_poppy_emergence.csv](https://raw.githubusercontent.com/gzahn/biostats_data/main/data/dwarf_bear_poppy_emergence.csv)

#### Data from UVU alum Eli Hartung

#### Data were collected to study the recruitment characteristics of *Arctomecon humulis*, an endangered species endemic to Washington County Utah. The dwarf bear poppy grows on gypsum outcrops covered in cryptobiotic crusts. He collected data on roughly 200 seedlings from three populations at the square foot plot and emergence point levels.

#### Response variable is binary (TRUE/FALSE) and predictors are categorical (suitable for logistic regression?)

##### Main question(s):

-	How does ground cover (substrate) and topography predict whether dwarf bear poppies will grow?

-	Do different genetic populations of dwarf bear poppy have different preferred growth requirements?

- Can we predict the probability of poppy presence in a given substrate/topography/population combination?

<br>

Variables:

+ **population**  Main genetic population, named by general location - Categorial - beehive, red dome, white bluff

+ **topography**  Topgraphy of location - Categorical - gradual, flat, steep

+ **substrate** Type of ground cover investigated - Categorical - cryptobiotic, large gravel, small gravel, gypsum, plant, bare soil

+ **emergence** Response variable - Whether a dwarf bear poppy was observed emerging from the random sampling location - Boolean

[Visualization](https://raw.githubusercontent.com/gzahn/biostats_data/main/figs/dwarf_bear_poppy_predictions.png)







___


### [data/coral_microbiome_metadata.csv](https://raw.githubusercontent.com/gzahn/biostats_data/main/data/coral_microbiome_metadata.csv) & [data/coral_microbiome_response.csv](https://raw.githubusercontent.com/gzahn/biostats_data/main/data/coral_microbiome_response.csv)

#### These two data files are microbiome data from coral reefs in the remote Chagos Archipelago.

#### The response "variable" is technically a matrix in the file data/coral_microbiome_response.csv

(we typically use ordinations and PermANOVA to model community structure)

#### Rows are samples, columns are observed bacterial orders

#### Values are relative abundance of each bacterial order in a given sample

<br>

112 samples

7 predictors

89 responses (bacterial orders)

<br>

#### Main question(s):

-	Does coral bleaching status have an effect on bacterial diversity?

-	Does location (leeward, windward) on a given island affect the bacteria that are present?

-	Do different host coral species harbor significantly different bacterial communities?

-	Is location (island, GPS, or exposure) more important than host species and health of the coral reef for determining which bacteria are present?

<br>

#### Response(s) are found in data/coral_microbiome_response.csv

#### Predictors are found in data/coral_microbiome_metadata.csv

Variables:

+ SampleID	Unique sample name (matches to first column of response table)

+ Date		Collection date (YYYY-MM-DD)

+ Island		Name of island collection was taken from - Categorical

+ Lat		Latitude (decimal degree)

+ Lon		Longitude (decimal degree)

+ Exposure	Site feature (leeward, windward, lagoonal) - We've seen before that this is oddly predictive of bacterial community structure

+ Host_Species	Latin name of host coral that the samples were taken from (P. acuta, P. damicornis)

+ Colony_Color	Ordered category - Healthy > Pale > Very pale > Bleached (as corals get sick they gradually become bleached) - stand-in for coral health

<br>

[Visualization](https://raw.githubusercontent.com/gzahn/Chagos/master/output/figs/acuta_and_damicornis_taxa_differential_abundance_combined_plot.png)