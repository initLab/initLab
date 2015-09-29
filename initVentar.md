# initVentar

Our beloved hackerspace is full of devices, tools and all kinds of other stuff, most of it with unknown owner and unclear hacking policy. An asset management system would be handy for keeping a database of init Lab's assets. This document will describe a basic feature list which could be used for building such an asset management system.

## Asset management

The asset management itself is nothing more than a library-like asset database with a proper UI for adding, removing and borrowing assets. It should be connected with Fauna for unified user/permission management.

Key features for the asset management module of initVentar:
- Add/remove asset [only by board members];
- Borrowing assets to initLab members;
- Asset properties:
  - Owner
  - Responsible person (shorter?) email
  - Hackable
  - Movable
  - Barcode (TYPE-IDXXXXX)
  - Brand
  - Model
  - Description
 
## Label printing

Printing meaningful asset labels is a feature important enough to be separated in another module. This module's features could include:
- Different label designs
  - Device
  - Toolset / toolbox
  - Place (shelf / case / whatever)
  - Price (for the kitchen)
- Static images, graphics and text
- Dynamic data from selectable database tables/fields
- Configurable label paper (size, label quantity, spacing, etc)
- Selectable starting label (for semi-used label papers)
- Selectable dynamic label quantity (like 'quantity' database field)

initVentar is being discussed in [issue 81](https://github.com/initLab/initLab/issues/81) in initLab's issue tracker.


