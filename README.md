def get(prompt):
    s = input(prompt).strip()
    return float(s) if s else None

v = get("Voltage (V): ")
i = get("Current (A): ")
r = get("Resistance (ohm): ")

if v is None and i is not None and r is not None:
    print(f"V = {i * r:g} V")
elif i is None and v is not None and r:
    print(f"I = {v / r:g} A")
elif r is None and v is not None and i:
    print(f"R = {v / i:g} ohm")
else:
    print("Leave exactly one value blank (and avoid dividing by zero).")
