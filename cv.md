Mihail Tereshhenko
---

**m.tereshhenko@yahoo.com**
*+79096166666*

- My main goal on the course is to structure everything I know about programming, learn a real programming language and enjoy the knowledge. I have long wanted to try web development, especially the backend (node.js), to participate in the development of something grandiose. Perhaps get a new profession.

- Of programming languages, I know only 1C and OOP patterns well. A bit of SQL, C #, Python.

- Sample code:

```csharp
static void Main(string[] args)
        {
            WriteLine("------ Fun with Data Readers ------- ");
            using (SqlConnection connection = new SqlConnection())
            {             
                var cnStringBuilder = new SqlConnectionStringBuilder
                {
                    InitialCatalog = "AutoLot",
                    DataSource = ".\\SQLEXPRESS",
                    ConnectTimeout = 30,
                    IntegratedSecurity = true
                };
                connection.ConnectionString = cnStringBuilder.ConnectionString;
                connection.Open();
                ShowConnectStatus(connection);
                string sql = "Select * from Inventory; Select * from Customers";
                SqlCommand myCommand = new SqlCommand(sql, connection);
                using (SqlDataReader myDataReader = myCommand.ExecuteReader())
                {
                    do
                    {
                        while (myDataReader.Read())
                        {
                            WriteLine("---Record---");
                            for (int i = 0; i < myDataReader.FieldCount; i++)
                            {
                                WriteLine($"{myDataReader.GetName(i)}: {myDataReader.GetValue(i)}");
                            };                    
                        }
                    } while (myDataReader.NextResult());
                }
                connection.Close();
                ShowConnectStatus(connection);
            }
   }

```

- I have 13 years of experience in the development of ERP systems based on 1C. The last place of work was an Italian cattle slaughter plant, where I wrote a program to record production.

- Higher education, math teacher. There are also certificates for 1C and BOSH.

- English - A1.