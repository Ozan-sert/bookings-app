# Bookings and Reservations

This project is a bookings and reservation system for a Bed & Breakfast. Visitors can search for accommodations by date and make an online reservation, while the site owner can manage reservations from a secure back end.

## Technologies Used
[![Version](https://img.shields.io/badge/goversion-1.16.x-blue.svg)](https://golang.org)
<a href="https://golang.org"><img src="https://img.shields.io/badge/powered_by-Go-3362c2.svg?style=flat-square" alt="Built with GoLang"></a>

The project is built in Go version 1.16.x and uses the following dependencies:
- chi router
- alex edwards SCS session management
- nosurf
- pgx
- simple mail
- Go validator

## Features
- Search for available accommodations by date
- Make online reservations
- Protection against Cross-Site Request Forgery (CSRF) attacks with nosurf middleware
- Email notifications for new reservations and reservation changes using simple mail package
- Responsive web design with Bootstrap to ensure a consistent user experience across devices

## Getting Started

To build and run this application, follow the steps below:
1. Install Soda by running `go install github.com/gobuffalo/pop/...`
2. Create a PostgreSQL database
3. Fill in the correct values in `database.yml`
4. Run `soda migrate` to migrate the database
5. Build and run the application by executing the following command from the root level of the project:
   ```
   go build -o bookings ./cmd/web/ && ./bookings \
   -dbname=bookings \
   -dbuser=postgres
   ```
   Make sure to replace `dbname` and `dbuser` with the correct entries for your database name and user. For a full list of command flags, run `./bookings -h`.

## Additional Features

The following features can be added to this bookings and reservation system:
- Ability to manage multiple properties
- Ability to manage multiple rooms within a property
- Integration with payment gateway to process payments
- Integration with mapping service to display location and directions
- Ability to send email reminders to guests prior to check-in
- Integration with a review system for guests to leave feedback on their stay.
