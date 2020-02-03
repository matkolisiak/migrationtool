# RescoCloud - Migration Tool
This document describes how to start up with Migration Tool in RescoCloud.
You can find implementation of this feature in AdminConsole -> Environnment section

# Content:
1. Clone Organization
2. Connect Organization
3. Disconnect Organization
4. Pull From

## Clone Organization
The main purpose of this button is to create a copy of your organization. You are able to customize which data of entities will be cloned too. 

1. Navigate to AdminConsole -> Environments (left side at the bottom)

2. Click on command item: Clone Organization (top of the page)

3. You should be navigate to another page, fill in informations about
e.g Organization: testenvironment-clone, e-mail: martin.liscinsky@resco.net, passw: test
	- Organization name: you need to define organization name as parentname-[customname]
	- Use the checkboxes for including/not inlcluding data of entities
4. Click on Save & Close (top of the page)

5. After a while you should be navigate back to page: Environments

6. The list of connected environments should be actualized and connection with cloned organization should be added (testenvironment-clone)

7. Check if cloned organization was created correctly 

8. Sign out

9. Log in to cloned organization
	- Organization name: testenvironment-clone (or your own organization)
	- E-mail: martin.lisicnsky@resco.net 
	- Password: test

10. Open Admin Console

11. Check if metadata and data was cloned correctly: 
	- Manage Data 
	- Entities

*Note:* Step 12. is not implemented yet. For completing step 12 (creating connection to parent organization), follow the instructions in `Connect Organization` section.

12. Navigate to Environments (left side ath the bottom) and you should be able to see a list of connected organizations, „parent“ of this organization should be visible in the list


## Connect Organization
The main purpose of this button is to create connection between two organizations.

1. Navigate to AdminConsole -> Environments (left side at the bottom)

2. Click on command item: Connect Organization (top of the page)

3. You should be navigate to another page, fill in information about organization, which you want to connect (System admin login required)
	- Organization name: testenvironment-clone (or your own organization)
	- E-mail: martin.lisicnsky@resco.net 
	- Password: test
	- Category: chose any
	- Description: add some description

4. Click on Save & Close (top of the page)

5. You should be navigated back to page: Environments

6. The list of connected environments should be actualized and new connection added

7. You are able to provide migration of metadata/data from connected organization. See `Pull From` section.


## Disconnect Organization
The main purpose of this button is to delete connection between two organizations.

1. Navigate to AdminConsole -> Environments (left side at the bottom)

2. You should be able to see a list of connected environments (organizations)

3. Check a checkbox in this list for unconnect

4. Click on command item: Disconnect Organization (top of the page)

5. You should be navigate to another page, click on Save & Close (top of the page)

6. You should be navigate back to page: Environments

7. The list of connected environments should be actualized and connection should be deleted


## Pull From Organization
The main purpose of this button is to import data|metadata|localizations from connected organization. You are able to accept or reject changes in your schema.
It is necessary to have 2 organizations created and also to have connection between them.

1. Navigate to AdminConsole -> Environments (left side at the bottom)

2. You should be able to see a list of connected environments (organizations)

3. Check a checkbox in this list of connected environments (organizations)

4. Click on command item: Pull From (top of the page)

5. You should be able to see menu with two options: Schema only; Custom

*Note:* Follow the instructions in the next two sections.

### Pull From- Schema Only

6. Click on Schema Only

7. After a while you should be navigate to page where are differences in metadata between these two organizations visualized

8. You are able to:
	- Check the checkoxes for entities/attributes  
	- Select a mode: Import/Update

*Note:* by checking/unchecking checkboxes you accept or reject changes after pulling from (which entity or attribute will be changed) 

*Note:* if you check entity && uncheck all its attributes => its like you accept all changes of entity

9. Click on Save & Close (top of the page)

10. After a while you should be navigate to Environments 


### Pull From - Custom

6. Click on Custom

7. You should be navigate to page, where you are able to select what should be pulling from connected environment (Schema|Localization|Data)

8. Feel free to check checkboxes on your feelings

9. Click on Pull From (top of the page)

10. After a while you should be navigate to page, where are differences between these two organizations visualized

11. You are able to:
	- Check the checkoxes for entities/attributes  
	- Select a mode: Import/Update
	- See number of entities which data will be imported

*Note:* by checking/unchecking checkboxes you accepting or rejecting changes after pulling from (which entity or attribute will be changed)

*Note:* if you check entity && uncheck all its attributes => its like you accept all changes of entity

12. After a while, you should be navigate to Environments
