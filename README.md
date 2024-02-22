## MECP Price Comparator Project

MECP (Mid East Canadian Pharmaceutical) is an online pharmaceutical retailer looking to enhance its market competitiveness by implementing an efficient algorithm to compare product prices with those of its competitors, Life Supply and Medical Warehouse. The objective is to accurately identify price discrepancies for identical or similar products based on their SKUs (Stock Keeping Units), despite variations in SKU formats and product quantities across different websites.

### Problem Statement

The project is divided into two primary components:

1. **Data Collection**: Develop scripts to extract product details, including SKUs and prices from the websites of the three companies: mecp.ca, medicalwarehouse.ca, and lifesupply.ca. This step involves navigating through the complexities of differing SKU formats and product quantities.

2. **Data Analysis and Comparison**: Implement an efficient algorithm to accurately match products across the providers by SKU and compare their prices, taking into account the quantity in which each product is sold.

### Challenges

- **SKU Variation**: Identical products may have SKUs that differ in prefixes, use of hyphens, or underscores across different websites. A key challenge is to standardize and match these SKUs accurately.
  
- **Price and Quantity Discrepancy**: The price listed for a product may represent a single unit or a case, which varies across websites. The algorithm must adjust for these differences to ensure a fair price comparison.

### Dataset Specifications

Each provider's dataset will contain a list of medical products with the following attributes:

| Column        | Details                                                       |
|---------------|---------------------------------------------------------------|
| SKU           | Unique code to identify the product                           |
| Price         | Price of the product (may represent a single unit or a case)  |
| Description   | Detailed product information, including name and colors       |
| Brand         | Brand name of the product                                     |
| Packaging     | Packaging type (single unit or a case)                        |
| Availability  | Product availability status                                   |

### Data Preprocessing

Data normalization is a crucial step before comparing SKUs. This includes removing spaces and non-alphanumeric characters from SKUs to facilitate accurate distance calculations.

### Comparison Approaches

- **Levenshtein Distance**: This algorithm will measure the similarity between MECP SKUs and those of competitors. Optimizations may be necessary to scale this approach for large datasets.

- **Cosine Similarity**: By converting SKUs into non-zero vectors, we can calculate the cosine similarity between the MECP SKU vector and competitor SKU vectors. A method for encoding SKUs into vectors will be developed as part of this approach.

After identifying matching products, we will compare their prices, taking product quantity into account to ensure an accurate comparison.
