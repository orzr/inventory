# inventory
A framework for easily keeping track of physical items

## Example use cases
* Know what is in the fridge
* Know if I have a certain tool and where to find it
* Know which foods are going to expire soon
* Avoid buying stuff which I already posses
* Describe my physical items and find them by properties e.g. weight or value
* Find staff which is never used
* Plan what needs to be bought and what is already available for a project

## Architecture
The two main entities are physical **items** and physical **locations**. There should be no strict model for neither items and locations. Both may be described e.g. by a document in a noSQL database.

Locations may be a room, a shelf, a fridge, a box, a truck, a container and airplane and many more.

An item can just be anything you want to keep track off, a screw, a can of milk, a tool, a car, a house an airplane and many more.

A server is responsible for storing the inventory database and for ensuring that no data loss or integrity violation occurs. Multiple clients may connect to the server, this implies that the server must ensure the ACID principles of databases.

Clients are responsible for scanning the items, e.g. via image recognition, barcode, QR-code, manual input. A client may be a Smartphone, a desktop computer, or a purpose build pice of hardware e.g. a robotic shelf.

## Key principles
* Simplicity for the user when puting items in the inventory
* Simplicity for the user when finding items in the inventory
* Data integrity
