# Profiles REST API

Creating a REST API in Python to manage users Profiles.
The application also consists of a TokenAuthentication functionality


## Functions of the API:

### 1. Create new profiles
    -> Handle registration of new users
    -> Validate profile Database

### 2. Listing existing profiles
    -> Search for profiles
    -> Email and name

### 3. View specific profiles
    -> Profile ID

### 4. Update profile of logged in user
    -> Change name, email and password

### 5. Delete Profile



## URLs of the API:

### 1. /api/profile/
    -> List all profiles when HTTP GET method is called
    -> Create new profile when HTTP POST method is called

### 2. /api/profile/<profile_id>/
    -> View specific profile details by using HTTP GET
    -> Update object using HTTP PUT / PATCH
    -> Remove it completely using HTTP DELETE




## Functions of Feed API:

    -> Creating new feed items -- Logged in users only
    -> Update feed items -- Logged in users only
    -> Deleting profile feed items -- Logged in users only
    -> Viewing other profile status updates -- All users




## URLs of the Feed API:

### 1. /api/feed/
    -> list all feed items
    -> GET (list feed items)
    -> POST (create feed item for logged in user)

### 2. /api/feed/<feed_item_id>/
    -> manage specific feed items
    -> GET (get the feed item)
    -> PUT/PATCH (update feed item)
    -> DELETE (delete feed item)





admin id -- gauty22@gmail.com
password -- 12345

profile ID -- gauty22@gmail.com
profile password -- password@123
