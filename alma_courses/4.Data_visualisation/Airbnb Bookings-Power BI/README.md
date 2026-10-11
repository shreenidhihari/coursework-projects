# Airbnb Booking Analysis

<br>

## 📄Problem Statement
To create a interactive dashboard of the Airbnb listings in Chicago & NewOrleans city by analysing various factors such as pricing, revenue, reviews, availability, location of the listings.

<br>

## 🎯Objective
To improve occupancy, profitability and user experience of the Airbnb listings based on the insights gained from the dashboard.

<br>

## 🔢Dataset
Airbnb booking dataset for Chicago & New Orleans is sourced from the [Airbnb Data](https://insideairbnb.com/get-the-data/)

- **Listing  Identifiers**: `id` `listing_url` `scrape_id` `last_scraped` `source` `name` `description` `neighborhood_overview` `picture_url` `neighbourhood_cleansed`  `latitude` `longitude`  `property_type`  `room_type`  `bathrooms`  `bedrooms` `amenities` `accommodates`.    
- **Listing Stay**: `minimum_nights` `maximum_nights`  `availability_30`  `availability_60`   `availability_90`   `availability_365` `instant_bookable`. 
- **Listing Revenue**: `estimated_revenue_l365d`  `price`.
- **Listing Reviews**: `number_of_reviews` `number_of_reviews_ltm`  `number_of_reviews_l30d`  `number_of_reviews_ly` `review_scores_rating` `review_scores_accuracy`  `review_scores_cleanliness`  `review_scores_checkin`   `review_scores_communication`  `review_scores_location`   `review_scores_value` `reviews_per_month`  `first_review`   `last_review`.   
- **Host**:  `host_id` `host_url` `host_name` `host_since` `host_location` `host_about` `host_response_time` `host_response_rate` `host_acceptance_rate` `host_is_superhost`  `host_thumbnail_url` `host_picture_url` `host_neighbourhood` `host_listings_count`  `host_total_listings_count`  `host_verifications`  `host_has_profile_pic` `host_identity_verified`  `calculated_host_listings_count` `calculated_host_listings_count_entire_homes` `calculated_host_listings_count_private_rooms`   `calculated_host_listings_count_shared_rooms`.    

<br>

### **Dataset Description**
- `id` `listing_url` `name` `picture_url` `description` `neighbourhood_cleansed` `neighborhood_overview` `latitude` `longitude` - Listing Identifiers as id, profile url, name, picture, description, neighbourhood name, neighbourhood details, location.
-  `property_type`  `room_type`  `bathrooms`  `bedrooms` `amenities` `accommodates` - Listing features such as property type, room type, count of bathrooms, bedrooms, other amenities and the occupancy size.
-  `minimum_nights` `maximum_nights`  `availability_30`  `availability_60`   `availability_90`   `availability_365` `instant_bookable` - Stay features included in minimum and maximum stay duration, availability based on last 1 month, 2 month, 3 month, 1 year and nature of booking(Instant Bookability).
- `estimated_revenue_l365d` `price` - Commercial features of listing such as revenue and price.
- `number_of_reviews` `number_of_reviews_ltm` `number_of_reviews_l30d` `number_of_reviews_ly` `reviews_per_month`- Number of Reviews of the rental listing in total, last 1 year, last 30 days, and reviews per month.
- `review_scores_rating` `review_scores_accuracy`  `review_scores_cleanliness`  `review_scores_checkin`   `review_scores_communication`  `review_scores_location`   `review_scores_value`- Review score of each listing based on rating, accuracy, cleanliness, checkin, communication, location, value parameters.
- `first_review` `last_review` - First & last review date of the listing.
- `host_id` `host_url` `host_name` `host_about` `host_thumbnail_url` `host_has_profile_pic` `host_picture_url` `host_location` `host_neighbourhood` `host_since`  `host_is_superhost` `host_verifications`  `host_identity_verified` - Host Identifiers including id, profile url, name, host description picture, location , neighourhood, years since host residence, Host Type(SuperHost, Non-SuperHost), Host verification details.
- `host_total_listings_count` `calculated_host_listings_count` `calculated_host_listings_count_entire_homes` `calculated_host_listings_count_private_rooms`   `calculated_host_listings_count_shared_rooms` - count of listings owned by hosts in total, count of listings owned by hosts based on room type.
- `host_response_time` `host_response_rate` `host_acceptance_rate` - Host Activity such as response time, response rate and acceptance rate.

<br>

## 🧹Data Cleaning & Transformation
- Converting Columns to Appropriate Data Types 
    - `host_response_rate` `host_acceptance_rate` - Datatype converted from text to percentages.
    - `price` - Datatype converted from text to number.
- Created New Columns
    - `city` - Created a city column to identify whether the city is Chicago or NewOrleans.
- Replacing categorical values
    - `host_is_superhost` - True/False entries are replaced with the SuperHost/Non-SuperHost values.
    - `host_identity_verified` - True/False entries are replaced with the Verified/Unverified values. 
    - `instant_bookable` - T/F entries are replaced with the True/False values.       

<br>

## 📁 Repository Structure
```
📦 Airbnb Bookings-Power BI
├──input/
│  ├──chicago_listings.csv
│  ├──new_orleans_listings.csv
├──screenshot/
│  ├──Listings.png
│  ├──New_Orleans_Listings.png
├──airbnb_dashboard.pbix
├── 📄 README.md
```

<br>

## Dashboard Preview
![Dashboard]()

<img width="1280" height="720" alt="image" src="https://github.com/shreenidhihari/coursework-projects/blob/a12b6aef818ce7119ef77c63ed26d07c2c2a665a/alma_courses/4.Data_visualisation/Airbnb%20Bookings-Power%20BI/screenshot/Listings.png" />

<br>

## Dashboard Usage
To view the dashboard, follow these steps:
- Clone this repository to your local machine.
- Open the `.pbix` dashboard file using PowerBI Desktop.
- Connect the dashboard using the dataset provided in repository.
- Explore the different pages and visuals within the dashboard to gain insights.
