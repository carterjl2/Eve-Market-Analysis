# Eve-Market-Analysis
Monitor data from Eve API and analyze/compile data of interest


Parameters:
char_name 	        required Your character name, so that I can contact you in case something goes wrong
buysell 	          required "s" for sell orders, "b" for buy orders, "a" for both
type_ids 	          Which type_id's to check
marketgroup_ids	    Which marketgroup_id's to check
region_ids 	        Which region_id's to check (optional, default is Jita only)
solarsystem_ids	    Which solarsystem_id's to check
station_ids 	      Which station_id's to check
minmax 	            Get the min or max values for an area. minmax=min, or minmax=max
callback 	          The JSONP callback function (optional, only needed for JSONP)

At least one from type_ids, marketgroup_ids, or region_ids is required.
a max of 10,000 rows will be returned


Return Values
(for .txt requests, this is the column order)

buysell 	        b or s
typeID 	          eve_inv_types.type_id
regionID 	        eve_map_regions.region_id
price 	          the price if 5% of the region's items for sale were bought
updated 	        date it was last updated, yyyy-mm-dd hh:mi:ss


Example URLs:

    http://eve-marketdata.com/api/item_prices2.txt?char_name=demo&type_ids=34,12068&region_ids=10000002&buysell=s - TXT format
    http://eve-marketdata.com/api/item_prices2.xml?char_name=demo&type_ids=34,12068&region_ids=10000002&buysell=s - XML format
    http://eve-marketdata.com/api/item_prices2.json?char_name=demo&type_ids=34,12068&region_ids=10000002&buysell=s - JSON format
