# car-management-software-Arabic


![Screenshot 2023-07-22 141830](https://github.com/khanfar/car-management-software-Arabic/assets/16803586/0cae1d7b-7be0-47a3-b710-7fa47260d8da)



![Screenshot 2023-07-22 013635](https://github.com/khanfar/car-management-software-Arabic/assets/16803586/743f3981-6dd7-4970-99fe-b4bc271d06aa)

![Screenshot 2023-07-22 013817](https://github.com/khanfar/car-management-software-Arabic/assets/16803586/720e05c6-6930-4769-a744-7794bce86830)



This is a Python script for a truck management system. It uses SQLite for data storage and pandas for data manipulation and export. The script is designed to manage trucks and their maintenance records. Here's a breakdown of the main functionalities:

1. **Time Adjustment**: The `get_adjusted_time` function adjusts the current time based on a specified offset.

2. **License Key Validation**: The script has a simple license key validation system. It prompts the user to enter a license key and checks if it's in a predefined list of keys. If the key is valid, it's removed from the list and the remaining keys are saved to a file in binary format.

3. **Login System**: There's a simple login system that prompts the user to enter a password. The user has three attempts to enter the correct password.

4. **Database Connection**: The `create_connection` function establishes a connection to a SQLite database.

5. **Database Backup**: The `backup_database` function creates a backup of the database and saves it to a USB drive.

6. **Database Setup**: The `create_tables` function creates two tables in the database: `trucks` and `records`.

7. **Truck Management**: The script provides functions to add, update, delete, and list trucks. Each truck has an ID, plate number, owner name, driver name, truck type, and phone number.

8. **Record Management**: The script provides functions to add, update, delete, and list maintenance records. Each record is associated with a truck and includes a date and text.

9. **Data Export**: The script allows the user to export records to an Excel file or a text file.

10. **Search Function**: The `search_truck` function allows the user to search for a truck by its plate number.

11. **Main Function**: The `main` function is the entry point of the script. It creates the database tables, handles the login system, and provides a menu for the user to choose an operation.

This script also uses the `winsound` module to play a beep sound at various points, such as after completing an operation or when an error occurs.

Please note that this script is designed to run on a Windows system, as it uses Windows-specific features like the `winsound` module and Windows file paths.

 here's a breakdown of all the functions in the provided code:

1. `get_adjusted_time(offset_hours)`: This function takes an offset in hours as an argument and returns the current time adjusted by that offset in the 'Asia/Amman' timezone.

2. `int_to_binary_x2(number)`: This function takes an integer as an argument, converts it to binary, doubles it, and returns the result as a string.

3. `get_license_key()`: This function prompts the user to enter a license key. If the key is valid, it removes the key from the list of available keys, updates the license keys file, and returns True. If the key is invalid, it plays a beep sound and prompts the user to enter the key again.

4. `check_license()`: This function checks if a valid license key exists in the license keys file. If a valid key exists, it returns True. Otherwise, it returns False.

5. `login()`: This function prompts the user to enter a password. If the password is correct, it returns True. If the password is incorrect, it plays a beep sound and allows the user to try again up to three times.

6. `beep_sound()`: This function plays a beep sound.

7. `create_connection(db_file)`: This function creates a connection to an SQLite database.

8. `backup_database()`: This function backs up the database to a USB drive.

9. `create_tables()`: This function creates the 'trucks' and 'records' tables in the database if they don't already exist.

10. `add_truck()`: This function prompts the user to enter details for a new truck and adds the truck to the 'trucks' table in the database.

11. `update_truck()`: This function prompts the user to enter a plate number and new details for a truck and updates the truck in the 'trucks' table in the database.

12. `delete_truck(plate_number)`: This function deletes a truck from the 'trucks' table in the database based on the plate number.

13. `add_record()`: This function prompts the user to enter a plate number and record text, and adds a new record to the 'records' table in the database.

14. `update_record()`: This function prompts the user to enter a plate number and new record text, and updates a record in the 'records' table in the database.

15. `delete_record()`: This function prompts the user to enter a plate number and deletes a record from the 'records' table in the database.

16. `list_trucks()`: This function lists all trucks in the 'trucks' table in the database.

17. `display_record_box(record)`: This function takes a record as an argument and displays it in a box.

18. `list_records()`: This function lists records in the 'records' table in the database based on the user's choice.

19. `search_truck()`: This function prompts the user to enter a plate number and searches for a truck in the 'trucks' table in the database.

20. `print_truck(truck)`: This function takes a truck as an argument and prints its details.

21. `main()`: This is the main function that runs the program. It creates the tables in the database, prompts the user to log in, and then presents a menu of options to the user.

here's a full prompt that you could use to generate this code:

"Create a Python command-line application for managing a fleet of trucks and their maintenance records. The application should use SQLite for data storage and pandas for data manipulation and export. The application should include the following features:

1. The application should keep track of the current time, with the ability to adjust the time by a certain number of hours.

2. The application should require a license key to use. It should prompt the user to enter a license key and validate it. If a valid license key does not exist, the application should not run.

3. The application should have a login process.

4. The application should be able to play a beep sound.

5. The application should be able to create a connection to a SQLite database.

6. The application should be able to backup the database to a USB drive.

7. The application should create the necessary tables in the database if they don't exist.

8. The application should be able to add a new truck to the database.

9. The application should be able to update the information of a truck in the database.

10. The application should be able to delete a truck from the database based on its plate number.

11. The application should be able to add a new maintenance record for a truck.

12. The application should be able to update a maintenance record for a truck.

13. The application should be able to delete a maintenance record for a truck.

14. The application should be able to list all the trucks in the database.

15. The application should be able to display a single record box.

16. The application should be able to list records based on user's choice.

17. The application should be able to search for a truck in the database.

18. The application should be able to print the details of a truck.

19. The application should have a main function that handles the flow of the application. This function should create a connection to the SQLite database and then start the application.

20. The application should be able to run from the command line. The entry point of the application should be a block of code at the end of the script that checks if the script is being run directly (i.e., `if __name__ == "__main__":`) and then calls the main function to start the application."


يستخدم التطبيق SQLite لتخزين البيانات والباندا لمعالجة البيانات وتصديرها
يتضمن التطبيق الميزات التالية:
يتتبع التطبيق الوقت الحالي ، مع إمكانية ضبط الوقت بعدد معين من الساعات
يتطلب التطبيق مفتاح ترخيص لاستخدامه
يطالب المستخدم بإدخال مفتاح الترخيص والتحقق من صحته. في حالة عدم وجود مفتاح ترخيص صالحأ لا يتم تشغيل التطبيق
حتوي التطبيق على عملية تسجيل دخول.
التطبيق قادرًا على تشغيل صوت صفير
التطبيق قادرًا على إنشاء اتصال بقاعدة بيانات SQLite.
التطبيق قادرًا على نسخ قاعدة البيانات احتياطيًا إلى محرك أقراص USB.
إنشاء الجداول الضرورية في قاعدة البيانات إذا لم تكن موجودة.
التطبيق قادرًا على إضافة شاحنة جديدة إلى قاعدة البيانات.
التطبيق قادرًا على تحديث معلومات الشاحنة في قاعدة البيانات
التطبيق قادرًا على حذف شاحنة من قاعدة البيانات بناءً على رقم لوحتها.
التطبيق قادرًا على إضافة سجل صيانة جديد لشاحنة.
التطبيق قادرًا على تحديث سجل الصيانة للشاحنة.
التطبيق قادرًا على حذف سجل الصيانة لشاحنة.
التطبيق قادرًا على سرد جميع الشاحنات في قاعدة البيانات.
التطبيق قادرًا على عرض مربع تسجيل واحد.
التطبيق قادرًا على سرد السجلات بناءً على اختيار المستخدم.
التطبيق قادرًا على البحث عن شاحنة في قاعدة البيانات.
التطبيق قادرًا على طباعة تفاصيل الشاحنة.
للتطبيق وظيفة رئيسية تتعامل مع تدفق التطبيق. يجب أن تنشئ هذه الوظيفة اتصالاً بقاعدة بيانات SQLite ثم تبدأ التطبيق.
