# News Portal



News Portal is a project where we practice using REST API for querying and retrieving information.

## Prerequisites

    PostgreSQL
    Java JDK
    Gradle
    Git
   

## Technology

    Java & Gradle
    Spark
    Junit for testing
    PostgreSQL database

## Setup Guide



    Run sudo apt-get install postgresql postgresql-contrib libpq-dev in the terminal to install PostgreSQL in your device.
    Enter y when prompted Do you want to continue? [Y/n] and wait for the installation to complete.
    Create your own credentials with superuser capabilities with the same name as our login name by running sudo -u postgres createuser --superuser $USER
    Next, we’ll have to create a database with the same name as our login name by running sudo -u postgres createdb $USER
    Finally run psql in the terminal to connect to the server

Structure

    After running the psql command to connect to the server, proceed to create the database wildlife-tracker by executing the following command: create database news_portal;
    Follow it up with this following command to connect to the newly created database\c news_portal;
    Once connected, create the following tables by running these commands:

CREATE TABLE users (id serial primary key, name varchar, position varchar, role varchar, department varchar);
CREATE TABLE news (id serial primary key, title varchar, description varchar, type varchar, author varchar);
CREATE TABLE departments (id serial primary key, name varchar, description varchar, totalemployees int);
CREATE TABLE departments_users (id serial primary key, deptid int, userid int);
CREATE TABLE departments_news (id serial primary key, deptid int, newsid int, userid int);
CREATE DATABASE news_portal_test WITH TEMPLATE news_portal;

    The last command creates the test database that shall be used to run your tests on. insert \q to exit psql server.




## Live APP
[Click Here](https://newsportal-12.herokuapp.com/)


