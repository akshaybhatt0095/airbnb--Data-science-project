# Airbnb--Data-science-project

Airbnb is a two sided marketplace which matches guests to hosts. The booking flow at Airbnb is as follows: a guest
finds an available room (listing) that they like, and then they contact the host. Once the guest finds a listing they
are interested in, there are three ways to send the host an inquiry: ‘contact_me’, ‘book_it’, or ‘instant_book’
(detailed at the bottom of this document). Upon receiving the inquiry, the host can then decide whether or not to
accept the request (for ‘contact_me’ and ‘book_it’ methods -- `instant_book` is auto-accepted). The main goal at
Airbnb is to increase bookings on the platform.


### Goal: Grow bookings in Rio de Janeiro.
1. Identifying the key metrics to monitor the success in improving the guest host matching process by clearly defining the metrics and explaining the method of computation.
2. What areas should the company invest in to increase the number of successful bookings in Rio de Janeiro? 
3. What segments are doing well and what could be improved? 
4. Propose 2-3 specific recommendations (business initiatives and product changes) that could address these opportunities.
5. Demonstrate rationale behind each recommendation AND prioritize your recommendations in order of their estimated impact.
6. What other research, experiments, or approaches could help the company get more clarity on the problem?

Information: There are three ways to book a listing on Airbnb:
1) contact_me - The guests writes a message to the host to inquire about the listing. The host has the option
to 1) pre- approve the guest to book their place, or 2) they can reject, or 3) they can write a free text
message with no explicit acceptance or rejection. If the host pre- approves, the guest can then go ahead
and click to make the booking (but is not obligated to).
2) book_it - The guest puts money down to book the place directly, but the host has to accept the
reservation request. If the host accepts, the booking happens automatically. If you have used Airbnb
before, this shows up as a button labeled “Request to book”.
3) instant_book - The guest books the listing directly, without any need for the host to accept or reject
actively (it is auto -accepted by the host). This shows up as a button labeled “Book”.



### Dataset description:
Contacts - contains a row for every time that a user makes an inquiry for a stay at a listing in Rio de Janeiro.
● id_guest_anon - id of the guest making the inquiry.
● id_host_anon - id of the host of the listing to which the inquiry is made.
● id_listing_anon - id of the listing to which the inquiry is made.
● ts_interaction_first - UTC timestamp of the moment the inquiry is made.
● ts_reply_at_first - UTC timestamp of the moment the host replies to the inquiry, if so.
● ts_accepted_at_first - UTC timestamp of the moment the host accepts the inquiry, if so.
● ts_booking_at - UTC timestamp of the moment the booking is made, if so.
● ds_checkin_first - Date stamp of the check -in date of the inquiry.
● ds_checkout_first - Date stamp of the check- out date of the inquiry.
● m_guests - The number of guests the inquiry is for.
● m_interactions - The total number of messages sent by both the guest and host.
● m_first_message_length_in_characters - Number of characters in the first message sent by the guest, if a
message was sent
● contact_channel_first - The contact channel through which the inquiry was made. One of {contact_me,
book_it, instant_book}. *See bottom of page for more detail*
● guest_user_stage_first - Indicates whether the user has made a booking before sending the inquiry (“past
booker”). If the user has not booked before, then the user is a new user.

Listings - contains data for every listing in the market
● id_listing_anon - anonymized id of the listing
● room_type - indicates whether the room is an entire home, private room, or shared room
● listing_neighborhood - the neighborhood of the listing
● total_reviews - the total number of reviews of the listing (at the time the data was pulled).

Users - contains data for every user
● id_user_anon - anonymized id of user
● words_in_user_profile - the number of words in the “about me” section of the user’s Airbnb profile (at
the time of contact)
● country - origin country of the user


<img src="https://github.com/akshaybhatt0095/airbnb--Data-science-project/blob/main/images/okr.png" width="1100" height="600">
<img src="https://github.com/akshaybhatt0095/airbnb--Data-science-project/blob/main/images/key%20metrics.png" width="1100" height="600">
<img src="https://github.com/akshaybhatt0095/airbnb--Data-science-project/blob/main/images/key%20metrics%20segmentation.png" width="1100" height="600">
<img src="https://github.com/akshaybhatt0095/airbnb--Data-science-project/blob/main/images/1.png" width="1100" height="600">
<img src="https://github.com/akshaybhatt0095/airbnb--Data-science-project/blob/main/images/2.png" width="1100" height="600">
<img src="https://github.com/akshaybhatt0095/airbnb--Data-science-project/blob/main/images/3.png" width="1100" height="600">
<img src="https://github.com/akshaybhatt0095/airbnb--Data-science-project/blob/main/images/4.png" width="1100" height="600">
<img src="https://github.com/akshaybhatt0095/airbnb--Data-science-project/blob/main/images/5.png" width="1100" height="600">
