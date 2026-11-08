# India new car prices and road tax by state (open data)

Free data from [CarUnbox](https://carunbox.com): the carmakers' own ex-showroom prices for every variant of 228 cars
from 24 brands, and what road tax, registration and insurance add in every Indian state.

## Files

| File | Rows | What is in it |
|---|---|---|
| `india-new-car-prices.csv` | 1,856 variants (1,701 with a price) | brand, model, variant, body, fuel, gearbox, the maker's ex-showroom price in rupees, main specs, the maker's page it came from, the CarUnbox page |
| `road-tax-by-state.csv` | 103 (3 example cars × the states with confirmed rules) | road tax with cess, registration, insurance, TCS and the on-road total, with links to the government documents the tax comes from |

## Where the numbers come from

- **Prices and specs:** only the carmaker's own website (its car page, price page and spec table). Never a dealer, a
  forum or another car site. `maker_page` is the page each row was read from. `price_region` is `India` when the maker
  publishes one price for the whole country, or the city the maker's price is for (`Delhi`).
- **Road tax:** each state's own Motor Vehicles Taxation Act, rules and notifications, read from the state's gazette or
  transport department. `tax_rule_sources` lists them. Registration fees follow the Central Motor Vehicles Rules;
  insurance follows the IRDAI third-party rates and the standard own-damage tariff; TCS is 1 % above ₹10 lakh.
- **Insurance and on-road totals are estimates.** A dealer's insurance quote and extra charges (fastag, accessories,
  handling) differ. The road tax is the rule applied to the example car; check the state's source for your own car.
- A blank cell means the maker does not publish that figure. Nothing is guessed or filled in.

## Columns

`india-new-car-prices.csv`: `brand, model, variant, body, fuel, transmission, ex_showroom_price_inr, price_region,
engine_cc, power_ps, torque_nm, mileage_kmpl, mileage_km_per_kg, battery_kwh, claimed_range_km, seats, length_mm,
width_mm, height_mm, wheelbase_mm, boot_litres, fuel_tank_litres, airbags, bharat_ncap_stars, maker_page,
carunbox_page`

`road-tax-by-state.csv`: `state, example_car, ex_showroom_price_inr, road_tax_inr, road_tax_percent_of_price,
registration_inr, insurance_inr, tcs_inr, on_road_price_inr, tax_rule_sources, rules_read_on`

The three example cars are a ₹8 lakh petrol car (1,197 cc, under 4 m), a ₹14 lakh diesel SUV (1,497 cc, over 4 m) and
a ₹14 lakh electric SUV (100 kW). Their prices sit away from the states' price slabs (₹5, 10, 15, 20 lakh), so no
example falls on a boundary. Sikkim has no row for petrol and diesel: its rule for them is not confirmed yet.

## Licence

[Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). Use it for anything,
including commercial work. Please credit: **Source: [CarUnbox](https://carunbox.com)**, with the link.

Car names and specs are the makers' facts; their trademarks belong to them.

## Updates

Rebuilt from the website's data after each price check. The on-road price of any car in any city:
[carunbox.com](https://carunbox.com).
