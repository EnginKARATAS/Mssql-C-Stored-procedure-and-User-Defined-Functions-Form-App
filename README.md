# Mssql C#Stored procedure and User Defined Functions Form App
 7th semester Stored procedure Mssql Functions  simple
 
 To Use 

<h1> Run these 3 code blocks from mssql</h1>

<h1>block one</h1>

CREATE TABLE [dbo].[Musteri]
(
[ID] [int] IDENTITY(1,1) NOT NULL,
[ADI] [varchar](50) NULL,
[SOYADI] [varchar](50) NULL,
[BAKIYE] [float] NULL
)
ON [PRIMARY]

<h1>block two</h1>

CREATE function Func_MusteriGetir(@username varchar(200))  
returns table  
as  
return (select * from Musteri where ADI = @username) 

<h1>block three</h1>

Create Proc Musteriler
@ID int,
@ADI varchar (50) output, <--
@SOYADI varchar (50) output<--
As
Select @ID=ID, @ADI=ADI,@SOYADI=SOYADI From Musteri Where ID=@ID

<h3>
and run into c#..
</h3>





