---
sidebar_label: 'Appendix B Sample ERD Exercises'
sidebar_position: 21
---

# Appendix B Sample ERD Exercises

## Exercise 1

### Manufacturer

 A manufacturing company produces products. The following product information 
 is stored: product name,
  product ID and quantity on hand. These products are made up of many 
  components. Each component can be
  supplied by one or more suppliers. The following component information is 
  kept: component ID, name,
  description, suppliers who supply them, and products in which they are 
  used. Use Figure B.1 for this
  exercise. 

 Create an ERD to show how you would track this information. 

 Show entity names, primary keys, attributes for each entity, 
 relationships between the entities and
  cardinality. 

### Assumptions

* A supplier can exist without providing components.
* A component does not have to be associated with a supplier.
* A component does not have to be associated with a product. Not all 
    components are used in products.
* A product cannot exist without components.

### ERD Answer

 Component(<u>CompID</u>, CompName, Description) PK=CompID 

 Product(<u>ProdID,</u> ProdName, QtyOnHand) PK=ProdID 

 Supplier(S<u>uppID</u>, SuppName) PK = SuppID 

 CompSupp(<u>CompID, SuppID</u>) PK = CompID, SuppID 

 Build(<u>CompID, ProdID</u>, QtyOfComp) PK= CompID, ProdID 

![component product ERD answer](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2013/12/Ch-16-Component-Product-ERD-Answer-300x160.jpg)

*Figure B.1 by A. Watt.*

## Exercise 2

### Car Dealership

 Create an ERD for a car dealership. The dealership sells both new and used 
 cars, and it operates a
  service facility (see Figure B.2). Base your design on the following 
  business rules: 

* A salesperson may sell many cars, but each car is sold by only one salesperson.
* A customer may buy many cars, but each car is bought by only one customer.
* A salesperson writes a single invoice for each car he or she sells.
* A customer gets an invoice for each car he or she buys.
* A customer may come in just to have his or her car serviced; that is, 
    a customer need not buy a
    car to be classified as a customer.
* When a customer takes one or more cars in for repair or service, one 
    service ticket is written for
    each car.
* The car dealership maintains a service history for each of the cars 
    serviced. The service 
    records are referenced by the car’s serial number.
* A car brought in for service can be worked on by many mechanics, and 
    each mechanic may work on many
    cars.
* A car that is serviced may or may not need parts (e.g., adjusting a 
    carburetor or cleaning a
    fuel injector nozzle does not require providing new parts).

### ERD Answer

![car dealership ERD](http://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2014/10/carDealership.png)
