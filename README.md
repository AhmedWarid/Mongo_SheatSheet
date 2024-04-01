# Mongo_SheatSheet
# MongoDB Command Cheat Sheet

## Database Operations
show dbs                   # List all databases
use <database_name>        # Create or switch to a database
db.dropDatabase()          # Delete the current database




## Collection Operations
show collections                 # List all collections in the current database
db.createCollection("<name>")    # Create a new collection
db.<collection>.drop()           # Drop/delete a collection




## CRUD Operations
db.<collection>.insert({...})                # Insert a new document
db.<collection>.insertMany([{...}, {...}])   # Insert multiple documents
db.<collection>.find()                       # List all documents in a collection
db.<collection>.find({...})                  # Query documents with conditions
db.<collection>.update({...}, {...})         # Update existing document(s)
db.<collection>.updateMany({...}, {...})     # Update multiple documents
db.<collection>.remove({...})                # Remove document(s) from a collection
db.<collection>.deleteMany({...})            # Delete multiple documents




## Query Operators
$gt, $gte, $lt, $lte       # Greater than, greater than or equal, less than, less than or equal
$ne                        # Not equal
$in, $nin                  # In, not in
$and, $or, $not            # Logical AND, OR, NOT
$exists, $type             # Check for existence, type
$regex                     # Regular expression match
$expr                      # Use aggregation expressions




## Update Operators
$set                       # Set a field value
$unset                     # Remove a field
$inc, $mul                 # Increment/decrement a field, multiply a field
$push, $pull               # Add to/remove from an array
$addToSet                  # Add a value to an array if it doesn't exist
$rename                    # Rename a field




## Indexing
db.<collection>.createIndex({...})        # Create an index on a field
db.<collection>.getIndexes()              # List all indexes on a collection
db.<collection>.dropIndex({...})          # Drop an index




## Aggregation
db.<collection>.aggregate([{...}, {...}]) # Perform data aggregation with pipeline stages
$match, $group, $sort, $project           # Common aggregation pipeline stages
$sum, $avg, $min, $max                    # Aggregation operators




## Administration
db.shutdownServer()                       # Shutdown the MongoDB server
db.getCollectionInfos()                   # Get information about collections
db.getCollectionNames()                   # Get names of collections
db.getFreeMonitoringStatus()              # Get free monitoring status
