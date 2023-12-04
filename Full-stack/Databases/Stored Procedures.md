#Databases 
![[Pasted image 20231011110441.png]]

- DELIMITER //
  CREATE PROCEDURE geAllProducts( )
  BEGIN
	  SELECT * FROM products;
  END//
  DELIMITER ;
![[Pasted image 20231011111932.png]]
- 