## MECP Price Comparator

MECP(Mid East Canadian Pharmaceutical) is a pharmaceutical company which sells medical products online. They want an efficient algorithm that will compare their product’s prices with two other competitors (Life Supply and Medical Warehouse) to show how they differ with cost.

### Problem Statement

Our project has 2 major parts involved, the first part is to create proper scripts which will find and collect SKU(Stock Keeping Unit) and prices of each product that all three companies share. These scripts will be along 3 websites, mecp.ca medicalwarehouse.ca and lifesupply.ca. The second part is once we have our data, to find an efficient algorithm to compare the different prices with the correct SKUs since our data size will be large.

Some of the problems to start are that some SKUs for the same product(across the websites) differ through how they may begin or how they use either hyphens or underscore characters to separate. So matching the SKUS properly would be done within the model. Another problem is the fact that the prices differ from the quantity of the product which is not consistent across the websites. Again with our model we’ll make it so that it properly matches prices with its quantity.

## Dataset

Dataset from each provider will contains list of medical products. Each product has following characteristics:

| Column | Details |
|--|--|
| SKU | Unique code to identify the product |
| Price | Price of the product. Price can be for a single unit or can be for a case |
| Description | Details of the product like name, colors and other characteristics |
| Brand | Brand name of the product |
| Packaging | Type of packaging. single unit or a case |
| Availability | If the product is available or not |

## Data cleanup

Data needs to be normalized before we can compute the similarities between SKUs. We will remove the space and any other non-alphanumeric characters from the SKUs before calculating the distances.

## Possible approaches

Following are the possible approaches for mapping similar SKU(s) that we are going to compare:

**Levenshtein Distance**: We'll use Levenshtein Distance to compare the similarity between MECP SKU and SKU of other product from different provider. This algorithm might not be feasible if we have millions of products. In this case we have to optimize the way we'll be comparing the words.

**Cosine similarities**: We'll create a non-zero vector from MECP SKU list and take a dot product with the target SKU vector. We have to figure out how we covert the word into vector (i.e. how will we encode the SKU into vector).

Once we found out the products that match the SKU, we will compare their prices. We'll take the quantity into the account to properly compare the prices.
