# Custom Stream

Integrate your own logging device with a custom **HTTP POST** to the **URL** you are given in the settings.

Use the following **JSON** format in the body of the **POST:**

```text
{
  "name": "YourDeviceName",
  "temp": 20.32,
  "aux_temp": 15.61, // Fridge or Room Temp
  "temp_unit": "C", // C, F, K
  "gravity": 1.042,
  "gravity_unit": "G", // G, P
  "pressure": 10,
  "pressure_unit": "PSI", // PSI, BAR, KPA
  "ph": 4.12,
  "comment": "Hello World",
  "beer": "Pale Ale"
}
```

Temperature units "**C**" for celcius, "**F**" for fahrenheit, "**K**" for kelvin.  
Gravity units "**G**" for SG and "**P**" for Plato.  
Pressure units "**PSI**", "**BAR**", "**KPA**".

**Never log more than once every 15 minutes**, request logged more often than that will be ignored.
