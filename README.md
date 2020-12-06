# Mssql C#Stored procedure and User Defined Functions Form App
 7th semester Stored procedure Mssql Functions  simple
 
 To Use 

<h1> run those two of block of code from mssql </h1>

CREATE function Func_MusteriGetir(@username varchar(200))  
returns table  
as  
return (select * from Musteri where ADI = @username) 
