# HW1-Movie-Kiosk
Guided software engineering tools practice 
Movie Theatre Ticker Kiosk
This toy system allows customers to view available movies and showtimes, choose an available seat, and purchase a ticket. The system then provides purchase confirmation and prevents the same seat from being sold twice. 

##Use Case: Purchase Ticket 
- Primary Actor: Customer
- Precondition: The kiosk is in use, at least one showtime for a movie has an available seat(s)
- Main Steps:
  1. The customer selects a showtime on the kiosk
  2. The Ticket Service provides available seats for that showtime to the Kiosk Interface to show the customer available seats queried from the seat database
  3. The customer selects the available seat(s) desired and the Ticket Service make the seats unavailable within the Seat Database while transaction is occurring, thus ensuring no duplicate purchases
  4. The customer enters payment information and the Payment Service processes this and approves or denies the purchase
  5. Once approved, the seats are marked as sold within the Seat Database and the Ticket Service sends a confirmation to the Kiosk Interface that shows confirmation to the customer  
- Post Condition: The ticket is issued, the selected seat(s) is marked as sold and cannot be purchased again for that showtime, and the customer has received a confirmation
