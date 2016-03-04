# -gtm-vendor-templates-Nanigans-commit-ae1d34c6961ef5067f6a6728d515
Below is an outline of how the data is passed in the nan_push function of the Javascript code.  It is needed to have a app_id, the client will be provided this when they start using Nanignas.  The code also needs a type and name.  

// NaN_api = [[app_id, user_id], [type, name, value, extra]];

   NaN_api.push([ {Nanigans site id}, {user id}], ['purchase', 'main', {value}, {'sku':{product_sku}, 'qty':{qty}, 'unique':{order_id}]);

As long as the //cdn.nanigans.com/NaN_tracker.js is called somewhere on the page the NaN_api.push can be used to send the information to Nanigans

Example
NaN_api.push([SITE_ID, uid], ['user', 'product_view', null,{'sku': 1173 }]);
