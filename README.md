![fireData](http://frapbot.kohze.com/SpatialMaps/SpatialMap_cover.jpg)
- Platform: http://www.SpatialMap.org 
- Docker: https://hub.docker.com/r/kohze/f8ff66a3b48e/
- R Package: https://github.com/SpatialMap/spatialmap

---

### About
The SpatialMap R package allows to manage SpatialMap user accounts and to update/upload/download pRoloc Datasets. This package is a fully integrated API connector to the SpatialMap platform and enables the programmatic access to all hosted datasets. 

### Setup
```
if (!require("devtools")) install.packages("devtools")
devtools::install_github("lgatto/spatialmap")

library(spatialmap)
```

### Examples
###### Loading pRolocdatasets
```
library(pRolocdata)
pRolocdata()
data("E14TG2aR")
```
###### Create a new account
```
createAccount()
```
###### Login (optional to receive token)
```
login()
```
###### Download Dataset (ID retrived from SpatialMap Platform)
```
object = download("-L-mRzp_fh6z1IdRQjWg")
```
###### Upload new dataset
```
upload(dataset = "E14TG2aR", name = "testData", public = FALSE)
```
###### Update existing dataset
```
update("E14TG2aR", name = "testMarch", randomKey = "-LFYwVIskvIQf-kCktgF", public = TRUE)
```
