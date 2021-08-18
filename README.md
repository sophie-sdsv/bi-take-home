# bi-take-home
**Take home challenge for BI Engineer position at Easyship**

**Thank you showing your interest in a position at Easyship. This take home challenge has set of scenario based questions, please try to solve them using SQL.**

Following are the table structure that will be required for assignment completion : 

Table containing list of all the clients Easyship has

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
| platform\_name            |
| currency                  |
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