# bi-take-home
**Take home challenge for BI Engineer position at Easyship**

**Thank you showing your interest in a position at Easyship. This take home challenge has set of scenario based questions, please try to solve them using SQL.**

---

Following are the tables that will be required for assignment completion : 

Table containing the list of all the clients at Easyship 

| es\_clients          |
| -------------------- |
| easyship\_client\_id |
| name                 |
| onboarding\_date     |
| country\_id          |
| classification\_id   |
| is\_active           |

Table containing list of all the couriers that are integrated with Easyship

| es\_couriers            |
| ----------------------- |
| easyship\_courier\_id   |
| name                    |
| courier\_umbrella\_name |
| supported\_services     |
| does\_pickup            |
| does\_tracking          |
| is\_active              |

Table containing shipment details

| es\_shipments             |
| ------------------------- |
| easyship\_shipment\_id    |
| easyship\_client\_id      |
| easyship\_courier\_id     |
| origin\_country\_id       |
| destination\_country\_id  |
| last\_status\_message\_id |
| label\_paid\_at           |
| total\_volumetric\_weight |

Shipment items table contains all the items within individual shipment

| es\_shipment\_items          |
| ---------------------------- |
| easyship\_shipment\_item\_id |
| easyship\_shipment\_id       |
| item\_category\_id           |
| volumetric\_weight           |
| contains\_battery            |

Status Records Table contain all the shipment tracking events 

| status\_records        |
| ---------------------- |
| status\_record\_id     |
| status\_message\_id    |
| easyship\_shipment\_id |
| created\_at            |

Status Messages is mapping table

| status\_messages    |
| ------------------- |
| status\_message\_id |
| name                |

Countries is a mapping table

| countries   |
| ----------- |
| country\_id |
| name        |
| region      |

---

Data can be accessed on BigQuery
: https://console.cloud.google.com/bigquery?project=easyship-staging-199203&p=easyship-staging-199203&d=data_test&page=dataset
Please reach out to HR if you do not have access

---

**Scenario :**

1. Operations Team would like to know what are the top 3 performing couriers in last 3 months. Performance is calculated based on the number of shipments. 


2. The pricing Team will be adjusting margin based on shipment volume.  Could you help them identify what was the % growth in terms of shipment last week compared to a week before? They would only like to see the result for these couriers umbrella names (FedEx and USPS). Week starts on Monday and ends on Sunday


3. Customer Success Team would like to know the average delivery times broken down by month and courier name for the last 3 months. Delivery time starts when a shipment has first status record event within (`In Transit to Customer, In Transit to Consolidation Center`) and Ends when there is first status record event within (`Delivered, Out for Delivery, Failed Delivery Attempt, Delivery Expected (End of Updates)`)


4. Business Team would like to know which couriers are used most on each day of the week. So the output will look like

| day\_of\_week | courier\_name                  |
| ------------- | ------------------------------ |
| Monday        | FedEx - International Priority |
| Tuesday       | DHL - Express Worldwide        |
| Wednesday     | USPS - First Class             |


5. Marketing Team would like to know, on average how much time does it take for a client to get activated. Activation Time is calculated from onboarding to the first shipment made


Good Luck and Feel free to reach out to HR in case of any queries.
