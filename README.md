# **Data Warehouse Modeling - Hospitality Business**

# **Business Process Mapping**

### **Key Processes on Hospitality Business:**

1. **Property Listing:**
    - Owners list their properties on the platform, providing details such as location, property type, amenities, photos, and prices.
2. **Search and Booking:**
    - Guests search for accommodations using filters such as location, stay dates, number of guests, and desired amenities.
    - After finding a suitable accommodation, guests make bookings, providing payment information and stay dates.
3. **Communication:**
    - Guests and property owners communicate through the platform to discuss reservation details, ask questions, and clarify doubts.
4. **Check-in and Check-out:**
    - Guests check-in to the reserved property, often using instructions provided by hosts.
    - After the stay, guests check-out and may leave reviews about the property and the host.

### **Dimensional Modeling of the Data Warehouse:**

A data warehouse (DW) for this business can be dimensionally modeled, which means that the data is organized into **dimensions** and **facts** and consistently serves an aspect for a DW.

Examples of important tables to consider:

1. **Dimensions:**
    - **DateDimension - Time Dimension:** Contains information about relevant dates for bookings, such as arrival date, departure date, and booking dates.
    - **LocationDimension - Location Dimension:** Details about the location of properties, including country, city, neighborhood, and geographical coordinates.
    - **BookingDimension - Booking Dimension:** Details of each booking, such as dates, stay period, and property type.
    - **PropertyDimension - Property Dimension:** Characteristics of the property, such as type (house, apartment, room), number of rooms, amenities, etc.
    - **GuestDimension - Guest/User Dimension:** Information about guests, such as age, gender, country of origin, etc.
    - **HostDimension - Host Dimension:** Details about property owners, such as name, location, number of listed properties, etc.
2. **Facts:**
    - **BookingFact - Booking Fact:** Contains information about bookings, such as booking ID, guest ID, property ID, relevant dates, price, etc.
    - **ReviewFact - Review Fact:** Stores guest reviews about properties and hosts, including ratings, comments, etc.
    - **CommunicationFact - Communication Fact:** Records interactions between guests and hosts, such as exchanged messages, dates, and relevant IDs.

**UML Chart:**
![Model](hospitality_dw_model.png)