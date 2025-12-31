# Agent Use Case: Music Store Insights with Chinook.db

## Product Value / Scenario
We are building an intelligent agent to help a music store make better business decisions and serve customers more efficiently. 
The store sells music albums and tracks to customers, tracks purchases via invoices, and has employees managing customer support. 
Our agent should help answer business questions, generate insights, and provide recommendations for both operations and marketing.

## Data We Have
The Chinook.db database contains 11 tables covering the full scope of the store’s operations:

- **Artist (275)** – Information about artists: `ArtistId`, `Name`.
- **Album (347)** – Albums linked to artists: `AlbumId`, `Title`, `ArtistId`.
- **Track (3503)** – Tracks with detailed info: `TrackId`, `Name`, `AlbumId`, `MediaTypeId`, `GenreId`, `Composer`, `Milliseconds`, `Bytes`, `UnitPrice`.
- **Genre (25)** – Music genres: `GenreId`, `Name`.
- **MediaType (5)** – Track media types: `MediaTypeId`, `Name`.
- **Customer (59)** – Customer info: `CustomerId`, `FirstName`, `LastName`, `Company`, `Address`, `City`, `State`, `Country`, `PostalCode`, `Phone`, `Fax`, `Email`, `SupportRepId`.
- **Employee (8)** – Employee info: `EmployeeId`, `LastName`, `FirstName`, `Title`, `ReportsTo`, `BirthDate`, `HireDate`, `Address`, `City`, `State`, `Country`, `PostalCode`, `Phone`, `Fax`, `Email`.
- **Invoice (412)** – Sales transactions: `InvoiceId`, `CustomerId`, `InvoiceDate`, `BillingAddress`, `BillingCity`, `BillingState`, `BillingCountry`, `BillingPostalCode`, `Total`.
- **InvoiceLine (2240)** – Invoice details: `InvoiceLineId`, `InvoiceId`, `TrackId`, `UnitPrice`, `Quantity`.
- **Playlist (18)** – Playlists: `PlaylistId`, `Name`.
- **PlaylistTrack (8715)** – Playlist-track mapping: `PlaylistId`, `TrackId`.

## Why Customers and Employees?
- **Customers** represent buyers and subscribers – their purchase behavior is crucial for recommendations and marketing.
- **Employees** include sales and support staff – useful for understanding support interactions, assigning reps, and evaluating employee performance.

## Value for the Agent
The agent can help the music store by:
1. **Customer Insights** – Recommend tracks/albums based on purchase history and popular genres.
2. **Sales Analysis** – Identify top-selling artists, albums, or tracks.
3. **Operational Support** – Suggest which employee should handle which customer, based on workload or expertise.
4. **Marketing & Promotions** – Target customers with offers based on purchase patterns or geographic trends.
5. **Playlist Recommendations** – Automatically generate playlists based on genre trends, artist popularity, or user preferences.

## Next Step (Agent Task)
- Ingest Chinook.db into the agent environment.
- Build the first task: **"Show the top 5 best-selling tracks and their corresponding artists."**
- This simple task allows the agent to demonstrate its ability to query relational data and provide actionable business insights.
