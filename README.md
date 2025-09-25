SQL Task 3 - Complete Solution
-- Create Database
CREATE DATABASE CompanyDB;
USE CompanyDB;
-- Create Tables
CREATE TABLE Employees (
 EmpID INT PRIMARY KEY AUTO_INCREMENT,
 FirstName VARCHAR(50),
 LastName VARCHAR(50),
 Department VARCHAR(50),
 Salary DECIMAL(10,2),
 HireDate DATE
);
CREATE TABLE Departments (
 DeptID INT PRIMARY KEY AUTO_INCREMENT,
 DeptName VARCHAR(50),
 Location VARCHAR(50)
);
-- Insert Sample Data
INSERT INTO Employees (FirstName, LastName, Department, Salary, HireDate) VALUES
('John', 'Doe', 'IT', 60000, '2022-05-15'),
('Alice', 'Smith', 'HR', 50000, '2021-08-20'),
('Bob', 'Brown', 'Finance', 70000, '2020-11-10'),
('Emma', 'White', 'IT', 65000, '2023-02-12'),
('David', 'Black', 'Sales', 55000, '2022-07-25');
INSERT INTO Departments (DeptName, Location) VALUES
('IT', 'Mumbai'),
('HR', 'Delhi'),
('Finance', 'Bangalore'),
('Sales', 'Pune');
-- Queries
SELECT * FROM Employees;
SELECT FirstName, LastName, Salary FROM Employees;
SELECT * FROM Employees WHERE Department = 'IT';
SELECT * FROM Employees WHERE Department = 'IT' AND Salary > 60000;
SELECT * FROM Employees WHERE FirstName LIKE 'A%';
SELECT * FROM Employees WHERE Salary BETWEEN 55000 AND 65000;
SELECT * FROM Employees ORDER BY Salary DESC;
SELECT * FROM Employees ORDER BY HireDate DESC LIMIT 3;
SELECT DISTINCT Department FROM Employees;
SELECT FirstName AS 'First Name', Salary AS 'Monthly Salary' FROM Employees;
