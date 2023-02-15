# Address Book

#### By Amanda Guan

#### An address book application using constructors and prototypes.

## Technologies Used

- Javascript
- HTML
- Git

## Description

An address book application using constructors and prototypes made during Week 4 of Epicodus Coding School, "Intermediate Javascript."Allows a user to enter Contact information, save it and display it. Editing features were started but not yet fully functional.

## Setup/Installation Requirements

- Copy the Repo Down
- Open the link and catalog your contacts!
- More functionality can always be added, like multiple options for address, types of contact [work, personal, etc.]! There's no such thing as too much organization!

## Known Bugs

- None

## License

MIT

Copyright (c) 2023 Amanda Guan

# TDD:
// Contacts  Business Logic

Describe: Contact()
Test: 'It will create a new contact returned with first name, last name, and phone number'
Code: let contact1 = new Contact('Jennifer', 'Bordon, '123-456-7890'); AddressBook(contact1) 
Output: contact1 = {
  firstName = Jennifer,
  lastName = Bordon,
  phoneNumber = 123-456-7890
}

// AddressBook Business Logic

Describe: addContact 
Test: "It should add contact." 
Code:
let addressBook = new AddressBook(); //create an AddressBook object.
let contact = new Contact("Ada", "Lovelace", "503-555-0100"); //create a new Contact object with a firstName of "Ada", saved to the variable name contact
let contact2 = new Contact("Grace", "Hopper", "503-555-0199");//create another new Contact object, this time with a firstName of "Grace", saved to the variable name contact2
addressBook.addContact(contact);// add the first Contact object to our AddressBook, using our new AddressBook.prototype.addContact() method
addressBook.addContact(contact2);//add the second Contact object to the AddressBook using the same new method
//Viewing Contact
addressBook;
addressBook.contacts;//To access these contacts
addressBook.contacts["Ada"];//Access contact1//In quotation
//addressBook.contacts["Ada"].phoneNumber;
Output: 
addressBook.contacts;//addressBook is an object that contains another object called contacts
AddressBook {
    contacts{//firstName as ID
        Ada: Contact,
        Grace: Contact
    }
}

Describe: assignId 
Test: "It should add an id to contact" 
Code: contact.id;
Expected Outcome: 1

Describe: findContact  
Test: "It should find a contact based on its id" 
Code: addressBook.findContact(2);
Expected Output: Contact {firstName: "Grace", lastName: "Hopper", phoneNumber: "503-555-0199", id: 2}

Describe:   AddressBook.prototype.deleteContact = function(id)
Test: "It should delete a contact by id" 
Code: AddressBook.prototype.deleteContact(0) 
Expected Output: AddressBook {Contact: {...}}
