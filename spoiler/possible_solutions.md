
# Identify Bounded Contexts

- Login, Offering, Enrollment, Ordering, Payment, Fulfillment, Invoicing, Reporting(s)

# Possible solutions (from the first run of the kata)

- Extract Item.views into Redis or into a dedicated Event table or into an Event DB
- Do we really need the watermarked item? just having it in a cache could be enough
- Remove link to Item in Download_limit
- Remove link to customer_id
- Extract schematic files into a S3 or cache for just a few hours
- Consider merging Watermarker_Item & Download_Limit since they're pretty much 1-1
- Decoupling bounded context requires decoupling identity: -> introduce Item_code, eg ISBN...or UID
- Keep Bundle & Items separate in Catalog & Offering, but it's all Item only in Fulfillment.
- Separate Fulfillment from Ordering etc. and remove watermarked_item_id from Order_Item
- Split User into 4+: User in Account / login, Customer in Enrollement & Reporting, Seller in Offering
- Update Item.view only from time to time (batched update) not in real-time 
- Extract Order.Status to a separate UX context 
