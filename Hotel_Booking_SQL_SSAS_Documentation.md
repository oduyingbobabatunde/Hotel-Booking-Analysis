# Hotel Booking Demand Project
## SQL Server and SSAS Multidimensional documentation

**Project:** BabatundeAssignment2  
**Database:** HotelBookingDB  
**Cube:** Hotel Booking DB  
**Confirmed source records:** 119,390

## Project overview

This project stores hotel booking data in SQL Server and analyzes it with an SSAS Multidimensional cube developed in Visual Studio. The cube uses the `HotelBookingsData` source table and supports analysis by hotel, market segment, country, arrival date, and hotel booking attributes.

## SQL Server source

The `HotelBookingDB` database contains two distinct tables visible in SSMS: `dbo.HotelBookings` and `dbo.HotelBookingsData`. The SSAS data source view uses **`dbo.HotelBookingsData`**. This table has a `BookingID` column in addition to the booking attributes. Examples of visible fields include `hotel`, `is_canceled`, `lead_time`, `arrival_date_year`, `arrival_date_month`, `stays_in_weekend_nights`, `stays_in_week_nights`, `adults`, `children`, `country`, `market_segment`, `adr`, and `total_of_special_requests`.

The following validation query returned **119,390** rows:

```sql
SELECT COUNT(*) AS TotalBookings
FROM HotelBookingDB.dbo.HotelBookingsData;
```

## Visual Studio and SSAS model

The Visual Studio solution and project are named **BabatundeAssignment2**. Solution Explorer shows:

| Component | Name |
| --- | --- |
| Data source | Hotel Booking DB.ds |
| Data source view | Hotel Booking DB.dsv |
| Cube | Hotel Booking DB.cube |
| Dimensions | Hotel.dim; Market segment.dim; Country.dim; Arrival Date.dim; Hotel Bookings Data.dim |

The data source view contains one displayed source table, `HotelBookingsData`; it shows no joins to separate dimension tables. The cube has one measure group, **Hotel Bookings Data**.

| Cube measure | Cube measure |
| --- | --- |
| Stays In Weekend Nights | Stays In Week Nights |
| Adults | Children |
| Adr | Total Of Special Requests |
| Number of Bookings | Total ADR |
| Number of Cancellations | |

The Dimension Usage screen shows **Hotel**, **Market segment**, **Country**, **Arrival Date**, and **Hotel Bookings Data** connected to the measure group. Each relationship cell displays **Booking ID**. These dimensions were created from attributes in the source table.

## Validation

The SQL row count is **119,390**. The cube Browser's **Number of Bookings** grand total was checked by the project owner and matches that count. This confirms the overall booking count is consistent between the SQL source and cube at the time checked.

## Analysis and Excel

The assignment also includes cube analysis questions and Excel charts. Their individual results and visuals are outside this draft because they have not been reviewed here. This document records the verified SQL Server and Visual Studio stages only.
