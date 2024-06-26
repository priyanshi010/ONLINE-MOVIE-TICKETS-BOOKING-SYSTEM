# ONLINE-MOVIE-TICKETS-BOOKING-SYSTEM

ABSTRACT
●The online movie ticket booking system is a web-based application that
simplifies the process of purchasing movie tickets for users and provides an
efficient platform for movie theaters to manage their ticketing operations.
The system allows users to search for movies, view movie details, select
showtimes, choose seats, and purchase tickets online. The system also
includes a back-end management system for theaters to manage their ticket
inventory, showtime scheduling, and sales reports. The system is built using
modern web technologies and is designed to be scalable, secure, and easy to
use. Overall, the online movie ticket booking system aims to provide a
seamless and convenient movie ticket booking experience for users and
theatre alike.
●The purpose of this document is to present a detailed description of the
Movie Ticket Booking System. It will explain the purpose and features of
the system, the interfaces of the system, what the system will do, the
constraints under which it must operate and how the system will react to
external stimuli.


SCHEMA DIAGRAM
![image](https://github.com/priyanshi010/ONLINE-MOVIE-TICKETS-BOOKING-SYSTEM/assets/124420981/8030c510-1c70-49ee-89af-64d1fde28460)

FUNCTIONAL REQUIREMENTS
● User Registration
Users should be able to register for the system by providing their name,
email, and password.
● Movie Search
Users should be able to search for movies based on movie title, genre, and
release date. The search results should include movie details such as plot
summary, cast, and crew information.
● Showtime Selection
Users should be able to select a showtime for a specific movie, and the
system should display the available seats for that showtime.
● Seat Selection
Users should be able to select seats from a seating chart and add them to
their shopping cart. The system should prevent double booking of seats.
● Ticket Purchase
Users should be able to purchase tickets using a credit or debit card. The
system should send a confirmation email to the user with their ticket details.
● Ticket Cancellation
Users should be able to cancel their ticket purchases and receive a refund.
● Theater Management
The theater management system should allow theaters to manage their
movie listings, showtimes, and ticket inventory. The system should generate
sales reports for theaters.

DDL COMMANDS:
Here are the examples of the tables and their corresponding columns for an
online movie ticket booking system:
1. tbl_bookings
● `book_id`
● `ticket_id,
● `t_id`
● `user_id`
● `show_id`
● `screen_id`
● `no_seats`
● `amount`
● `ticket_date`
● `date`
● `status`
2. tbl_contact
● `contact_id`
● `name`
● `email`
● `mobile`
● `subject`
3. tbl_login
● `id`
● `user_id`
● `username`
● `password`
● `user_type`
4. tbl_movie
● `movie_id`
● `t_id`
● `movie_name`
● `cast`
● `desc`
● `release_date`
● `image`
● `video_url`
● `status`
5. tbl_news
● `news_id`
● `name`
● `cast`
● `news_date`
● `description`
● `attachment`
6. tbl_registration
● `user_id`
● `name`
● `email`
● `phone`
● `age`
● `gender`
7. tbl_screens
● `screen_id`
● `t_id`
● `screen_name`
● `seats`
● `charge`
8. tbl_shows
● `s_id`
● `st_id`
● `theatre_id`
● `movie_id`
● `start_date`
● `status`
● `r_status`
9. tbl_theatre
● `id`
● `name`
● `address`
● `place`
● `state`
● `pin`
These tables represent the core entities of an online movie ticket booking
system, including users, movies, theaters, showtimes, seats, and tickets.

DML COMMANDS:
-
-- Indexes for table `tbl_bookings`
--
ALTER TABLE `tbl_bookings`
ADD PRIMARY KEY (`book_id`);
--
-- Indexes for table `tbl_contact`
--
ALTER TABLE `tbl_contact`
ADD PRIMARY KEY (`contact_id`);
--
-- Indexes for table `tbl_login`
--
ALTER TABLE `tbl_login`
ADD PRIMARY KEY (`id`);
--
-- Indexes for table `tbl_movie`
--
ALTER TABLE `tbl_movie`
ADD PRIMARY KEY (`movie_id`);
--
-- Indexes for table `tbl_news`
--
ALTER TABLE `tbl_news`
ADD PRIMARY KEY (`news_id`);
--
-- Indexes for table `tbl_registration`
--
ALTER TABLE `tbl_registration`
ADD PRIMARY KEY (`user_id`);

-- Indexes for table `tbl_screens`
--
ALTER TABLE `tbl_screens`
ADD PRIMARY KEY (`screen_id`);
--
-- Indexes for table `tbl_shows`
--
ALTER TABLE `tbl_shows`
ADD PRIMARY KEY (`s_id`);
--
-- Indexes for table `tbl_show_time`
--
ALTER TABLE `tbl_show_time`
ADD PRIMARY KEY (`st_id`);
--
-- Indexes for table `tbl_theatre`
--
ALTER TABLE `tbl_theatre`
ADD PRIMARY KEY (`id`);
--
-- AUTO_INCREMENT for dumped tables
--
--
-- AUTO_INCREMENT for table `tbl_bookings`
--
ALTER TABLE `tbl_bookings`
MODIFY `book_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=15;
--
-- AUTO_INCREMENT for table `tbl_contact`
--
ALTER TABLE `tbl_contact`
MODIFY `contact_id` int(11) NOT NULL AUTO_INCREMENT;
--
-- AUTO_INCREMENT for table `tbl_login`

--
ALTER TABLE `tbl_login`
MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=20;
--
-- AUTO_INCREMENT for table `tbl_movie`
--
ALTER TABLE `tbl_movie`
MODIFY `movie_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=18;
--
-- AUTO_INCREMENT for table `tbl_news`
--
ALTER TABLE `tbl_news`
MODIFY `news_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=11;
--
-- AUTO_INCREMENT for table `tbl_registration`
--
ALTER TABLE `tbl_registration`
MODIFY `user_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;
--
-- AUTO_INCREMENT for table `tbl_screens`
--
ALTER TABLE `tbl_screens`
MODIFY `screen_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=7;
--
-- AUTO_INCREMENT for table `tbl_shows`
--
ALTER TABLE `tbl_shows`
MODIFY `s_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=23;
--
-- AUTO_INCREMENT for table `tbl_show_time`
--
ALTER TABLE `tbl_show_time`
MODIFY `st_id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=22;
--
-- AUTO_INCREMENT for table `tbl_theatre`
--
ALTER TABLE `tbl_theatre`
MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=7;

TOOLS AND TECHNOLOGY REQUIRED
The tools and technologies used for developing an online movie ticket
booking system can vary depending on the specific requirements and
preferences of the development team. Here are some commonly used tools
and technologies for building an online movie ticket booking system:
1. Programming Languages:
The system can be built using a combination of programming languages
such as HTML, CSS, JavaScript, Node.js, and Python.
2. Web Frameworks:
Web frameworks such as Express.js, Flask, and Django can be used for
developing the application layer of the system.
3. Database Management System:
Database management systems such as MongoDB, MySQL, and
PostgreSQL can be used for storing and managing data in the data layer of
the system.
4. Payment Gateway:
A payment gateway such as UPI payment, Debit/Credit card can be
integrated into the system to facilitate secure online payments.
5. API Integrations:
API integrations with third-party services such as movie databases, location
services, and notification services can enhance the functionality of the
system.
