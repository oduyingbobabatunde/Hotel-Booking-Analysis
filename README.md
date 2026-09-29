# Hotel Booking Analysis

A hotel booking analysis project built with SQL Server, SQL Server Analysis Services (SSAS) Multidimensional, Visual Studio, and Excel.

## Project workflow

1. Store and inspect hotel booking records in SQL Server.
2. Build an SSAS Multidimensional cube in Visual Studio.
3. Explore booking measures by hotel, market segment, country, and arrival date.
4. Present the analysis in Excel.

## Data and model

- **SQL database:** `HotelBookingDB`
- **Cube source table:** `dbo.HotelBookingsData`
- **Source records:** 119,390
- **Visual Studio solution:** `BabatundeAssignment2`
- **SSAS cube:** `Hotel Booking DB`
- **Dimensions:** Hotel, Market segment, Country, Arrival Date, and Hotel Bookings Data

The cube includes measures for booking count, cancellations, average daily rate (ADR), total ADR, guest counts, nights stayed, and special requests. The cube's **Number of Bookings** grand total matches the 119,390 rows counted in the SQL source table.

## Documentation

See [SQL Server and SSAS project documentation](Hotel_Booking_SQL_SSAS_Documentation.md) for the confirmed source, cube structure, dimensions, measures, and validation. The individual assignment answers and Excel charts can be added as the analysis is documented.
