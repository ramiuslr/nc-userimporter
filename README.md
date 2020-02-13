# About nc-userimporter

This tool creates Nextcloud users from a CSV file, which you exported from some other software or created with a spreadsheet software.

Zip files with executables for Windows, MacOS, Linux available here: https://get.edudocs.org/de/assets/nc-userimporter/ - If you have a Python3 environment with all the dependencies/modules installed, you can run the script without the build of course.

Screenshot input:
![Screenshot from Windows commandline](https://github.com/t-markmann/nc-userimporter/blob/master/assets/screenshot.png)

## Instructions

1. Download and extract the zip-file for your operating system from https://get.edudocs.org/de/assets/nc-userimporter/

2. Insert data:
    * __config.xml__: Insert your cloud-admin credentials into file _config.xml_. The user must have admin permissions in your Nextcloud.
    * __users.csv__: Insert the user data into the file _users.csv_ or recreate it with the same columns in a spreadsheet software.

    Avoid special characters in username and password (including german umlauts) or test if the character is allowed first.

3. Start the tool:
    * __Windows__: doubleclick _nc-userimporter.exe_.
		(built and tested with Win10 Pro 1803 64-bit)
	* __Linux__: doubleclick _nc-userimporter_ or via terminal: change to the app-directory and execute: ./nc-userimporter
		(built and tested with Ubuntu 16.04 x86_64; tested with Fedora 29 x86_64, openSUSE Leap 15.0 x86_64, Arch)
		__Troubleshooting__: Make sure the file is executable (https://www.qwant.com/?q=make%20file%20executable%20linux)
	* __Mac__: doubleclick _nc-userimporter_. Answer the prompt with "open", ignore the warning.
		(built and tested with macOS 10.12 Sierra)
		__Troubleshooting__: Make sure the file is executable (https://www.qwant.com/?q=make%20file%20executable%20mac)

4. Follow the interactive commandline instructions. Check output.log ("output"-folder in script-directory) and your user overview in Nextcloud.


## Output

Screenshot output:

![Generated PDF file with user credentials](https://github.com/t-markmann/nc-userimporter/blob/master/assets/screenshot_pdfoutput.png)

---

## ToDo

* improve documentation of features https://github.com/t-markmann/nc-userimporter/wiki#todo-documentation
* refactoring / clean code

Open features, not yet implemented (help appreciated): 
* Passwords with special characters not supported?
* add default language; for each user in users.csv? Or at least to config.xml. Else new users will always get english welcome mails.
* read config from CLI-input if config-file is empty; update config.xml with input values?
* ask if users exists first: https://docs.nextcloud.com/server/15/admin_manual/configuration_user/instruction_set_for_users.html
* add other userdata
