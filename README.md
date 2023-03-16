# FDS-Airbnb
Airbnb Dataset

Everybody (individuals or groups): We would like you to investigate what makes a good property for Airbnb in Edinburgh. How well can features of a property listing be used to predict its popularity or short-term rental price? Are particular areas or neighbourhoods more sought after or expensive than others?
Groups: The extra questions should extend the basic findings to explore advanced relationships in the data. Examples of questions are:
• Have you identified anything unusual about listings which suggest they are not genuine / true rentals?
• Some Airbnb hosts have multiple listings and may be running them as a business. Do their listings seem more popular than more hosts with single listings?
• The housing policies of cities and towns can be restrictive of short-term rentals, to protect housing for residents. Do features, such as the ‘minimum nights’ setting for listings reveal any patterns that may be indicative of such policies in particular neighbourhoods?
• Any other questions that arise as you explore the data.

<h3>Notes</h3>
1. listing_id in reviews.csv is a unique id for a property in listing.csv

<h5>Data Cleaning</h5>
<h3>Columns to remove in listing.csv</h3>
<ol>
<li>neighbourhood_group_cleansed (Check if the whole column is empty)</li>
<li>host_url</li>
<li>host_name</li>
<li>listing_url</li>
<li>scrape_id</li>
<li>last_scraped	</li>
<li>source</li>
<li>calendar_updated</li>
<li>calendar_last_scrapped</li>
</ol>


<h3>Modification</h3>
<ol>
    <li>picture_url to boolean (0,1)</li>
    <li>license (check what it is)</li>
    <li>Convert True and False to (0,1)
        <ul>
    <li>instant_bookable</li>
    <li>host_identity</li>
    <li>host_has_profile_pic</li>
    <li> host_is _super_host</li>
    <li>has_availabilty</li>
        </ul>
    <li>Remove % symbols
        <ul>
            <li>host_acceptance_rate</li>
            <li>host_response_rate</li>
        </ul>
    </li>
    <li>Convert property_type to some numbers</li>
    <li>Find unique values in room_type and assign numbers to it</li>
    <li>Seperate parking from description/name</li>
    <li>Remove html tags from the description</li>
</ol>

<h3>Modification done by abhay</h3>
<ol>
    <li>No need to change since no null values - deleting pictures_url</li>
    <li>deleting license column since only 15 entries has license</li>
    <li></li>
    <li></li>

</ol>

<h3>Clarification</h3>
<ol>
    <li>Bathroom</li>
</ol>

Question-1
We would like you to investigate what makes a good property for Airbnb in Edinburgh

1. Create new Dataframe - delete: description, overview, host_since, host_location, host_about, 'host_neighbourhood', 'host_verifications', 'neighbourhood', latitude, longitude, room_type, property_type, reviews_per_month 
2. Convert variables from host_response_time 
3. Check for zero or Nan in host_response_rate and host_acceptance_rate
4. host_has_super_host, bedrooms, beds to int from float
5. bathroom_txt to bathrooms, consider only nums 
6. Split amenities, only on keywords 
7. remove dollar sign in price
8. Remove rows with null in all review_scores columns
9. 


<h3>Links for similar projects</h3>
1. https://www.kaggle.com/code/duygut/airbnb-nyc-price-prediction
