--FROM  Customers c left join Orders o ON c.customer_id=o.customer_id
--left join Shippings s on c.customer_id=s.customer where s.status="Pending" AND o.amount>10;
--getting all hte uSA constumer 

--select first_name , last_name, country, age from Customers where age>25;
--select SUM(amount) 
--from Orders