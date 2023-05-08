Download Link: https://assignmentchef.com/product/solved-solvedc-project-solution
<br>
Instructions:For this assignment you will need the following classes: Weapon, Character, Armor, Helmet, and Chestpiece. You will also need an IEquippable interface with an Equip method that doesn’t return anything, but takes in a Character parameter. That Character class will need a string for a name, an int for base attack, a Weapon for currently equipped weapon, a List of IEquippables for the equippable inventory, and a Dictionary with string keys and Armor values for the currently equipped armor. The Weapon class needs to implement the IEquippable interface and contain an int member variable named attack. The Weapon’s implementation of the Equip method should make the Character parameter’s equipped Weapon member equal to this Weapon. The Armor class should be abstract, implement the IEquippable interface, contain an int for defense, and doesn’t necessarily need an implementation of the Equip method. The Chestpiece class should inherit from the Armor class and the Equip method should place this Chestpiece into the equipped armor Dictionary of the Character parameter with the key “Chestpiece”. The Helmet class should inherit from the Armor class and the Equip method should place this Helmet into the equipped armor Dictionary of the Character parameter with the key “Helmet”.The Program.cs Main method will be used to give the user access to this functionality. Similar to your earlier code exercises, you will need to give the user several options and accept input from the user for a selection. The Program will need a Character to be the target of these options. At a minimum, the following options will need to be available: create weapon, create armor, and equip. Creating either a Weapon or Armor should place the created object into the equippable inventory List of the target Character in Program. Equip should allow the user to choose any object in the equippable inventory of the Character and call that object’s Equip method giving it the target Character as the parameter, this should perform the appropriate method for equipping that object.An equipped object should no longer appear in the equippable inventory. Once the object is in the Dictionary it should be removed from the List. If an object is attempting to be equipped to a location that is already occupied (equipped Weapon already exists, or key in Dictionary already exists) the object currently occupying that space should be placed in the equippable inventory List before being replaced by the new object.

The following guidelines are the grading categories for this assignment:

Class Creation

Create an IEquippable interface that contains an Equip method with no return value that accepts a Character parameter.Create an abstract class called Armor that derives from IEquippable and has a member int called defense.Add a List member variable that contains the type IEquippable to Character to act as the Character’s equippable inventory.Add a Dictionary member variable whose keys are strings and values are Armor to Character that will act as the Character’s currently equipped armor.Create a Helmet class and a Chestpiece class that both derive from Armor.

Dictionary Usage

Helmets are equipped by being placed into the Character parameter’s equipped armor Dictionary with the key “helmet”.Chestpieces are equipped by being placed into the Character parameter’s equipped armor Dictionary with the key “chestpiece”.Equipping Armor objects is done through the Equip method inherited from IEquippable.Character’s DisplayStatus method should include information about what Armor objects are currently equipped, referring to Armor in the Armor Dictionary, and the total defense of all equipped Armor.

List Usage

When an IEquippable is equipped(placed in the current armor Dictionary) it should be removed from the Character’s equippable inventory.When an IEquippable is going to be overwritten by a different object being equipped (ie. a Helmet being equipped when a Helmet is already equipped) the object being overwritten should then be stored in the Character’s equippable inventory.Weapons are also IEquippable so make sure that Weapons also operate correctly. Meaning they are added to and removed from the IEquippable inventory when swapping Weapons. This may require some changes and improvements to the Equip method for Weapons.

Main Menu Updates

The main menu will need some way of creating Helmets and Chestpieces that are placed in the mainCharacter’s equippable inventory.The main menu will need some way of creating some sort of Weapon and placing it in the mainCharacter’s equippable inventory (There is already a case that creates Weapons, you can probably just modify that one).The main menu will need a way for the user to select equippable objects to equip them from the main character’s equippable inventory.

Recommendations(not required)

Have a method in Character that displays the objects in the IEquippable list with their defense or attack values for use when the user must select from that inventory.Have a method in Character that displays what objects are in the equipped armor Dictionary along with their defense values for use in the DisplayStatus method.Have a method in Character that totals of the defense value of the equipped armor for use in the DisplayStatus method.Methods in Character for selecting from, adding to, and removing from the equippable inventory.

Extra InformationGo back through your code and check for the following:

All variables and methods are named appropriately.Member variables should have either protected or private access.Anytime the user is asked for input the expected input is made clear to the user.Any information being output to the user should be clear and concise.The user should be clearly informed of what is occurring throughout the application. When values change or objects are instantiated information about this occurrence should be displayed.Make sure that the program does not exit until the user chooses to exit and they can continue to select different options until they choose to exit.Make sure the user can’t select an option that accesses an object that doesn’t exist.Make sure that equipping a Weapon or Armor object doesn’t cause any object to no longer be accessible, it should either be in the inventory List, the equipped Dictionary, or the equipped Weapon.