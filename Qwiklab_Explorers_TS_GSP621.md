# Analyzing Billing Data with BigQuery || [GSP621](https://www.cloudskillsboost.google/focuses/7114?parent=catalog) ||

# # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 👍😄🤝

### Run the following Commands in CloudShell

```
bq query --use_legacy_sql=false \
'SELECT * FROM `billing_dataset.enterprise_billing` WHERE Cost > 0'

bq query --use_legacy_sql=false \
'SELECT
 project.name as Project_Name,
 service.description as Service,
 location.country as Country,
 cost as Cost
FROM `billing_dataset.enterprise_billing`;'

bq query --use_legacy_sql=false \
'SELECT
 project.name as Project_Name,
 service.description as Service,
 location.country as Country,
 cost as Cost
FROM `billing_dataset.enterprise_billing`;'

bq query --use_legacy_sql=false \
'SELECT project.id, count(*) as count from `billing_dataset.enterprise_billing` GROUP BY project.id'

bq query --use_legacy_sql=false \
'SELECT ROUND(SUM(cost),2) as Cost, project.name from `billing_dataset.enterprise_billing` GROUP BY project.name'
```

* Go to **BigQuery** from [here](https://console.cloud.google.com/bigquery?)

```
SELECT CONCAT(service.description, ' : ',sku.description) as Line_Item FROM `billing_dataset.enterprise_billing` GROUP BY 1
```
```
SELECT CONCAT(service.description, ' : ',sku.description) as Line_Item, Count(*) as NUM FROM `billing_dataset.enterprise_billing` GROUP BY CONCAT(service.description, ' : ',sku.description)
```

# Congratulations ..!!🎉  You completed the lab shortly..😃💯

# *Well done..!* 👏

# Thank you for visiting.... :) 🗯️

# [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN)
