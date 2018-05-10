CREATE USER 'pabloem'@'localhost' IDENTIFIED BY 'numbani*2131!';
GRANT ALL PRIVILEGES ON * . * TO 'pabloem'@'localhost';

wp search-replace 'https://pabloem.digital' 'http://pabloem.digital' --allow-root