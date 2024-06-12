Separate Fulfillment from Ordering etc.
- remove watermarked_item_id from Order_Item



Do we really need the watermarked item? just having it in a cache could be enough

Remove link to Item in Download_limit

Remove link to customer_id

Extract schematic files into a S3 or cache

Consider merging Watermarker_Item & Download_Limit since they're pretty much 1-1




Extract Item.views into Redis or a dedicated Event table or Event DB


Separate Fulfillment from Ordering etc.
- remove watermarked_item_id from Order_Item

Extract Item.views into Redis or a dedicated Event table or Event DB

Split User into 4+: 
- User in Account / login
- Customer in Enrollement
- Seller in Offering
- Customer in reporting

Keep Bundle & Items separate in Catalog & Offering, but it's all Item in Fulfillment.

Extract Item.views into Redis or a dedicated Event table or Event DB

Split User into 4+: 
- User in Account / login
- Customer in Enrollement
- Seller in Offering
- Customer in reporting

Keep Bundle & Items separate in Catalog & Offering, but it's all Item in Fulfillment.

Decoupling bounded context requires decoupling identity: -> introduce Item_code, eg ISBN...or UID


---

Item views updated in a differed way

