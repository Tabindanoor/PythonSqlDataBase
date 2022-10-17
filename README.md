# PythonSqlDataBaseDataFetching


# Importing module
import mysql.connector
import webbrowser
def main():
# Creating connection object
    connection = mysql.connector.connect(
    host = "database-2.cb9giyizmupx.ap-northeast-1.rds.amazonaws.com",
    port = 3306,
    user = "admin",
    password = "12345678",
    database="employee_schema"
)
 
    cursor = connection.cursor()
 # get the cursor
    cursor.execute('Select * from employee_schema.Persons;')
    
 # fetching data from tables
    
    extracted_data = cursor.fetchall()
    for i in extracted_data:
        print(i)

main()

