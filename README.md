# Simulating a fast-food environment

### Project Overview

RGyUm is a new initiative to improve access to fast-food options on campus by simulating a fast-food environment. The goal of this project is to design and implement a menu management and ordering system that allows for seamless interactions for both users and administrators. 



### Tool used
Python google Coolab 



### Data Sources

The simulator uses menu.csv and food.csv files to load initial data for menu items, categories, and product availability



### Data Cleaning and Preparartion

in the initial data preparation phase, I performed the following task
1. Data loading and Inspection
2. Standardising the column names
3. Merging the Datasets
4. Changing values in a data frame


### Technical Implementation
The program utilizes Python’s built-in libraries to handle data manipulation and user inputs. The core data is loaded from two .csv files, which are then merged into a data frame used to maintain and update menu items, stock, and pricing in real-time. The use of data frames enables efficient inventory tracking, allowing updates to reflect immediately in the user interface for a streamlined experience.


### Key Features and Program Options
#### 1. Admin Login:
  The admin login feature ensures only authorized personnel can manage the menu inventory. Upon selecting this option, admins are prompted to enter their credentials:

  - Username: Admin
  - Password: Any number smaller than 10 (including floats and negatives)
  - Attempts Allowed: 4
  - If all attempts fail, the program will lock out the user until it is restarted. Upon successful login, this option becomes disabled until the next program run.

#### 2. Add Products (Admin-Only):
Accessible only after a successful admin login, this option allows the admin to update the stock of existing menu items:

  - Admins can view the current list of menu items and input a menu number to add one product to a specific slot.
  - A maximum of 8 items per menu slot is enforced, with the program issuing a warning if the admin tries to add products beyond this limit or attempts to add items in empty slots.
  - Once completed, the program returns to the main menu, showing the updated stock.


#### 3. Buy Food (Available to All Users):
The buy food option allows any user to purchase available menu items. This includes:

  - A display of the menu, prices, and item availability for users to browse.
  - After selecting an item, the program displays its price and prompts for payment.
  - Payment simulation accepts any positive number and returns a message based on the amount entered:
    - If the payment exceeds the price, the program calculates and displays the change.
    - If the payment matches the price, a thank-you message is shown.
    - If the payment is insufficient, the user is asked to input additional funds.
  - Once purchased, the program updates the data frame to reflect the remaining inventory and prompts users if a selected item is out of stock.
#### 4. Exit:
Users can select this option to exit the program.

### Potential Use Cases
This simulation can be a valuable tool for:
  - Understanding menu and inventory management in fast-food settings.
  - Simulating user interaction scenarios for fast-food purchases.
  - Implementing user authentication and secure access to admin features in small applications.

