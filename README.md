Fuel Consumption Planner for 75hp 2-Stroke Outboard

Constants based on Nova's real data

LITERS_PER_KM = 1.04 LITERS_PER_NM = 1.91 DRUM_VOLUME = 200  # 1 drum = 200 liters

def calculate_fuel_by_distance(distance_km=None, distance_nm=None): if distance_km is not None: fuel_needed = round(distance_km * LITERS_PER_KM, 2) drums_needed = round(fuel_needed / DRUM_VOLUME, 2) return { "distance_km": distance_km, "fuel_liters": fuel_needed, "drums": drums_needed } elif distance_nm is not None: fuel_needed = round(distance_nm * LITERS_PER_NM, 2) drums_needed = round(fuel_needed / DRUM_VOLUME, 2) return { "distance_nm": distance_nm, "fuel_liters": fuel_needed, "drums": drums_needed } else: return "Please enter a distance in either kilometers or nautical miles."

Example Usage

trip1 = calculate_fuel_by_distance(distance_km=240)  # Kikori to Daru trip2 = calculate_fuel_by_distance(distance_km=40)   # Daru to Mabudawan

print("Trip 1 - Kikori to Daru:", trip1) print("Trip 2 - Daru to Mabudawan:", trip2)

Add more trips as needed below

e.g., print(calculate_fuel_by_distance(distance_nm=50))

