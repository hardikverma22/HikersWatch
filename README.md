# HikersWatch

Using Location and Geocoder Capability to show lattitude, longitude, Altitude and Address
<pre>
Geocoder geocoder = new Geocoder(getApplicationContext(), Locale.getDefault());
        try {
            String address="Could not find Address";

            List<Address> listAddresses = geocoder.getFromLocation(location.getLatitude(),location.getLongitude(),1);
            if(listAddresses!=null && listAddresses.size()>0) {
                address="";
                Log.i("place info", listAddresses.get(0).toString());

                if (listAddresses.get(0).getSubThoroughfare() != null && listAddresses.get(0).getSubThoroughfare() != "") {
                    address =address+", "+listAddresses.get(0).getSubThoroughfare();
                }
                if (listAddresses.get(0).getThoroughfare() != null && listAddresses.get(0).getThoroughfare() != "") {
                    address =address+", "+ listAddresses.get(0).getThoroughfare();
                }
                if (listAddresses.get(0).getLocality() != null && listAddresses.get(0).getLocality() != "") {
                    address = address+", "+listAddresses.get(0).getLocality();
                }
                if (listAddresses.get(0).getPostalCode() != null && listAddresses.get(0).getPostalCode() != "") {
                    address =address+", "+ listAddresses.get(0).getPostalCode();
                }
                if (listAddresses.get(0).getCountryName() != null && listAddresses.get(0).getCountryName() != "") {
                    address =address+", "+ listAddresses.get(0).getCountryName();
                }
                addresstextView.setText("Address : "+address);
            }
            
          </pre>
