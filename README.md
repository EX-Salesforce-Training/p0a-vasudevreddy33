![Revature Logo](./Revature%20Logo.png "Revature Logo")

# P0A-Requirements

## Postal Service
For part A of Project 0, you have two tasks: 
*	Construct a data model that supports a mailing company like the USPS while satisfying the requirements in the below Data Model; and
*	Configure proper security to satisfy the requirements listed in the below Security section.

Note, decisions made for either can and/or will affect potential decisions made in the other. For example, deciding to use a Master-Detail over a Lookup relationship will dictate what record-level security options are available for use on the child object. You should have a Lightning Application, called Postal Service that will contain your P0. For each object, you must also create a custom page layout, list view and if applicable, custom related list(s)/record type(s).

### Data Model
Your data model should consist of 5 objects: Mail, Address, Inhabitant, Contact, and Route. See the below requirements that should influence your decision on how to construct the data model. You should make your decision on what is presented.
* 	A single piece of mail should be aware of where it is going, who it is addressed to, its height, its width, its weight, if it’s fragile and its delivery status.
* 	Address should consist of individual fields for each address-item (i.e., street/city/state/zip code) and a single field that represents a whole-formatted address, named Mailing Address.
* 	A Driver (User) is assigned a Route at all times.
* 	Ideally, we’d like to keep track of which Drivers have been assigned to a Route.
* 	A Route can consist of multiple stops.
* 	Multiple people can live at one address.
* 	One person can have several properties. 

### Security
There are two users to your application. The Driver and the Mail Handler. See the below requirements that should influence your decision on how to configure your security settings. You should make your decision on what is presented.
* 	Drivers should not be able to create or delete Mail.
* 	Drivers are in charge of updating the delivered status of a piece of Mail but should not be able to edit the other fields.
* 	Mail Handlers should only be able to specify which Route a piece of Mail is assigned to.
* 	Neither User should be able to enter/change the Contact/Address/Inhabitant fields. We will assume that there is a third user (System Admin) that is in charge of inputting data in Salesforce.
* 	If a User cannot see a Contact, they should not be able to see the places in which they live.
* 	If a User cannot see an Address, they should not be able to see the people that live there.
* 	Users should only see the Postal Service Lightning Application.
* 	Users should only see relevant Tabs when viewing the Postal Service Lightning Application.
* 	Users should only be able to Login from 8AM-8PM.
