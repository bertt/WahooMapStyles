# Tags and values in Wahoo maps v23 (Utrecht)

The map tiles that a Wahoo ELEMNT downloads are [Mapsforge](https://github.com/mapsforge/mapsforge) `.map` files (stored as `.map.lzma`). Only the OSM tags that Wahoo wrote into the map can be matched in a style (`<m k="..." v="...">` in `vtm-elemnt.xml`). Many values are renamed by Wahoo, for example OSM `bicycle=no` becomes `bicycle=bic_no`. Use the values in this page, not the raw OSM values, in your style rules.

## How this list was made

- Source: the Wahoo Desktop map folder, map version `23`, the 19 tiles covering the Utrecht area (zoom 8 tiles `129..133` / `82..86`).
- Method: each tile is decompressed and the tag table in the Mapsforge header is read. Tags are listed separately for points (POI) and lines/areas (WAY).
- This is the **union of the tag tables** of those tiles. It shows which tags and values the map *can* contain, not how often they occur.
- Version `21` is almost identical. Version `23` adds `oneway:bicycle=ow_bic_no`.
- Reverse-engineered, not official Wahoo documentation.

## Cycling relevant (WAY)

| Tag | Values |
|---|---|
| `bicycle` | bic_yes, bic_designated, bic_permissive, bic_destination, bic_forestry, bic_permit, bic_private, **bic_no** |
| `oneway:bicycle` | ow_bic_no |
| `oneway` | yes, no, -1 |
| `cycleway_lane` | cw_lane_both/left/right/oneway/oneway_rev |
| `cycleway_track` | cw_track_both/left/right/oneway/oneway_rev |
| `cycleway_shared` | cw_shared_both/left/right |
| `cycleway_shoulder` | cw_shoulder_both/left/right |
| `cycleway:oneway` | cw_ow_no |
| `network` | lcn, rcn, ncn |
| `mtb_scale` | mtbs_0 to mtbs_6 |
| `mtb_scale_uphill` | mtbu_0 to mtbu_5 |
| `access` | acc_no, destination, forestry, permit, private |
| `foot` | ft_yes, ft_designated, ft_permissive, ft_destination, ft_permit, ft_private, ft_no |

## Roads and surface (WAY)

| Tag | Values |
|---|---|
| `highway` | motorway(_link), trunk(_link), primary(_link), secondary(_link), tertiary(_link), unclassified, residential, living_street, road, service, services, track, path, footway, pedestrian, cycleway, bridleway, steps, construction, raceway, bus_guideway, via_ferrata |
| `surface` | asphalt, paved, smooth_paved, rough_paved, compacted, gravel, unpaved, raw |
| `tracktype` | grade1 to grade5 |
| `trail_visibility` | excellent, good, intermediate, bad, horrible, no |
| `bridge` | yes, movable |
| `tunnel` | yes, no |
| `ford` | fd_yes |
| `toll` | tl_yes |
| `ladder`, `embankment`, `seasonal`, `intermittent`, `safety_rope`, `lock` | ld_yes, emb_yes, seas_yes, wwi_yes, sr_yes, yes |
| `area`, `area:highway` | yes, pedestrian |

## Nature and land use (WAY)

| Tag | Values |
|---|---|
| `natural` | beach, cliff, coastline, dune, fell, gorge, grassland, heath, nosea, reef, ridge, rock, sand, scree, scrub, sea, shingle, sinkhole, strait, tree_row, valley, water, wetland, wood |
| `landuse` | basin, brownfield, cemetery, farmland, forest, grass, greenfield, meadow, military, orchard, quarry, railway, recreation_ground, reservoir, village_green, vineyard |
| `leisure` | beach_resort, common, dog_park, garden, golf_course, nature_reserve, park, pitch, playground, slipway, sports_centre, stadium, swimming_area, swimming_pool, water_park |
| `waterway` | river, stream, canal, drain, dam, dock, lock_gate, rapids, waterfall, weir |
| `wood`, `leaf_type` | coniferous, deciduous, mixed; broadleaved, needleleaved, mixed, leafless |
| `boundary` | national_park, protected_area, maritime |
| `protect_class` | 1, 2, 4, 5, 6, 11, 21 |
| `protection_title` | Landschaftsschutzgebiet, Naturschutzgebiet, protected_site |
| `admin_level` | 1, 2, 4 |
| `border_type` | contiguous, eez |
| `location` | underground |

## Other (WAY)

| Tag | Values |
|---|---|
| `railway` | rail, light_rail, tram, subway, station, platform, funicular, narrow_gauge, miniature, preserved, abandoned, disused |
| `amenity` | bar, biergarten, bus_station, cafe, ferry_terminal, fountain, fuel, grave_yard, hospital, kindergarten, marketplace, parking, place_of_worship, police, recycling, restaurant, school, shelter, theatre, toilets, water_point |
| `barrier` | block, city_wall, fence, retaining_wall, wall |
| `sport` | climbing, golf, shooting, soccer, swimming, tennis |
| `piste:type`, `piste:difficulty`, `piste:grooming` | downhill, nordic, sled, hike; novice, easy, intermediate, advanced; classic, backcountry |
| `aeroway`, `aerialway`, `route`, `whitewater`, `place`, `religion`, `shelter_type` | aerodrome, helipad, taxiway; cable_car; ferry; portage_way; locality; christian, jewish; basic_hut, picnic_shelter, public_transport, weather_shelter |

## Points of interest (POI)

| Tag | Values |
|---|---|
| `amenity` | atm, bank, bench, bicycle_rental, bicycle_repair_station, bus_station, cafe, charging_station, cinema, compressed_air, doctors, drinking_water, fast_food, ferry_terminal, fountain, fuel, hunting_stand, kindergarten, library, marketplace, parking, pharmacy, place_of_worship, police, post_box, pub, recycling, restaurant, school, shelter, telephone, theatre, toilets, water_point |
| `shop` | bakery, beverages, bicycle, books, butcher, car, chemist, convenience, doityourself, hairdresser, laundry, motorcycle, organic, supermarket |
| `barrier` | block, bollard, border_control, chain, checkpoint, cycle_barrier, gate, kissing_gate, lift_gate, stile, turnstile |
| `bicycle`, `access`, `surface` | bic_yes/designated/permissive/destination/permit/private/no; acc_no, forestry, permit, private; asphalt, paved, compacted, gravel, raw, rough_paved, smooth_paved, unpaved |
| `highway` | bus_stop, emergency_access_point, ford, mini_roundabout, motorway_junction, passing_place, traffic_signals, turning_circle |
| `tourism` | apartment, attraction, camp_site, caravan_site, hotel, information, museum, picnic_site, viewpoint |
| `natural` | cape, cave_entrance, geyser, nat_stone, peak, saddle, sinkhole, spring, strait, tree, water, wood |
| `place` | country, state, city, town, village, hamlet, suburb, quarter, neighbourhood, island, locality, isolated_dwelling |
| `historic` | archaeological_site, boundary_stone, castle, memorial, monument, ruins, wayside_cross, wayside_shrine |
| `information` | board, guidepost, office, terminal |
| `man_made` | adit, cross, lighthouse, reservoir_covered, surveillance, survey_point, water_well, watermill, windmill, windpump |
| `waterway` | lock_gate, rapids, water_point, waterfall, weir |
| `leisure`, `memorial`, `emergency` | nature_reserve, picnic_table, playground, slipway, swimming_area; plaque, statue, stolperstein, stone, war_memorial; defibrillator, phone |
| `cycle_node`, `hike_node` | NLBE; rwn |
| `shelter_type` | lean_to, picnic_shelter, public_transport, rock_shelter, weather_shelter |
| `drinking_water` | yes, no |
| `railway`, `station` | crossing, halt, level_crossing, station, tram_stop; light_rail, subway |
| `aeroway`, `aerialway` | gate; station |
| `building`, `capital`, `boundary` | yes; 2, 4; protected_area |
| `ford`, `ladder`, `mountain_pass`, `summit:cross` | fd_yes, ld_yes, yes, yes |
| `generator:source`, `power`, `vending` | geothermal, hydro, solar, wind; generator; bicycle_tube |
| `landuse`, `military`, `religion`, `sport` | basin, forest; bunker; christian; climbing, swimming |
| `whitewater` | egress, put_in, put_in;egress |

## Example

Match ways where cycling is forbidden:

```xml
<m e="way" k="bicycle" v="bic_no">
    <!-- your line style here -->
</m>
```
