#installed the groq 
!pip install groq
#created the GROQ API key
import os
os.environ["GROQ_API_KEY"] = "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"
# Basic prompt using llama model
from groq import Groq

# Initialize client for API KEY
client = Groq(api_key=os.environ["GROQ_API_KEY"])

# Run a basic prompt
response = client.chat.completions.create(
    model="llama3-8b-8192",  # Replace with "gemini" if Groq hosts it
    messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "Can you able to create the location creation in the system"},
        {"role": "user", "content": """create location creation in the system by using below data
  Location_ID: 123
  Location_Name: Paris, France
  Country: France
  Region: Europe
  Latitude: 48.8566
  Longitude: 2.3522
  Address: Paris
"""}
    ]
)

print(response.choices[0].message.content)

#added the few field and saved in pdf 
import pandas as pd

warehouse_location_data = {
    "Location_ID": [101],
    "Location_Name": ["Main Warehouse - Section A"],
    "Warehouse_Code": ["MW-A"],
    "Capacity_SqFt": [5000],
    "Status": ["Active"],
    "Address": ["123 Industrial Road, Anytown, USA"],
    "Check_Sequence": [1],
    "Put_Sequence": [1],
    "Pick_Sequence": [1]
}

warehouse_location_df = pd.DataFrame(warehouse_location_data)
display(warehouse_location_df)
# saved in csv format
warehouse_location_df.to_csv('warehouse_locations.csv', index=False)
print("Warehouse location data saved to warehouse_locations.csv")
