# Assignment_IoTReady

# Install Frappe
pip install frappe-bench           

# Setup a Frappe Bench
bench init my_bench                
cd my_bench
bench new-site my_site
bench get-app frappe --branch version-13
bench --site my_site install-app frappe

# bench new-app link_bundler
bench new-app link_bundler          

# Define DocTypes
{
  "name": "Bundle",
  "description": "Link Bundle",
  "fields": [
  
    {
      "fieldname": "password",
      "label": "Password",
      "fieldtype": "Password",
      "reqd": 1
    }, 
]
}

{
  "name": "Link",
  "description": "Link in Bundle",
  "fields": [
    
    {
      "fieldname": "url",
      "label": "URL",
      "fieldtype": "Data",
      "reqd": 1
    },
    
  ]
}

# Define Python Logic
def create_bundle():        // for create page 

def view_bundle(bundle_id, password=None):         //for view page


