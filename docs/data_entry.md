
# Nursery Data Entry Workflow

## Accession and Receipt

- **Accession Creation**:
  - The accession technician receives a seed lot from a source.
  - An accession number is created for this material, and an accession card is printed.
  - The accession is given the item number `.99` along with the item status `Seed Store` as the first entry.
  
- **Receipt**:
  - The nursery receives an 8” x 5” heavy stock paper accession form from the accession technician, curator, or horticulturist with the seed packet attached.
  - Seed and cards are kept together in the seed store refrigerator.

## Processing

- **Seed Processing**:
  - Soon after receipt at the nursery, the seed is processed.
  - The seed is inspected visually, counted if possible, and cleaned if required.
  - The taxon is then ascribed a dormancy type based on research data or prior experience with nursery cultivation.
  - **Dormancy Types**: Morphophysiological (MPD), Morphological (MD), Physiological (PD), Physical (PY), and No Dormancy (ND).
  - Depending on the dormancy type and time of year, the taxon is given a treatment type and sowing date/location, noted on the accession card.
  - A production label is handwritten with the name, accession number, month to sow, and number of plants requested. The label is affixed to the seed packet and accession card.
  - Accessions with the same sowing date are bundled together and returned to the refrigerated seed store.

- **IrisBG Data Entry**:
  - Once the information is accumulated on the accession card, it’s time for IrisBG data entry.
  - The accession item number is set to `.88`, and the status is changed to `Prop: Processing`.
  - The month to sow, location to sow, a quick description of the treatment, and the dormancy type are added as comments in the Material section along with the desired number of plants requested.
  - The seed, card, and label are then placed back into the refrigerator.

## Culturing

- **Seed Cultivation**:
  - When the sowing date arrives, the accession is removed from the fridge for cultivation.
  - Seed treatments and treatment times vary by taxa. The seed is treated and sown as indicated on the accession card.
  - The card is stamped with the date sown and refiled.

- **IrisBG Data Entry**:
  - The item status is set to `Prop: Culturing`.
  - All treatments are considered and noted when possible.
  - Short-duration treatments (e.g., acid scarification or overnight soaking) are separated from longer treatments by date and entered as a separate sequential record.
  - Treatments of less than 24 hours may be given a different date for simplicity, but the actual treatment time is noted in the Propagation `Duration` cell.
  - **Details to Apply**: Propagule type, Quantity, Treatment, Environment, Medium, Container, and Duration (if applicable).
  - The dormancy type is added to the Propagation comments box (and removed from the Material comments).

## Germination

- **Daily Inspection**:
  - Seed pots are inspected daily.
  - Once seed germination is noticed, the germination date is written on the back of the production label in the format "G. day/month/year".
  - **Note**: Germination can be sporadic, especially with material from wild-collected populations; thus, the germination date can be idealized rather than the actual date.
  
- **IrisBG Data Entry**: Nothing at the time of germination.

## Pricking-Out

- **Procedure**:
  - The removal of seedlings from the communal seed pot into individual containers is referred to as ‘pricking-out’.
  - The accession card is removed from the 'ungerminated' card file and updated with the germination date, the number of plants pricked out, the new container size, and the planting medium used.
  - The accession card is then filed into the 'Germinated' drawer.

- **IrisBG Data Entry**:
  - Two sequential entries are made in IrisBG after pricking-out:
    1. **Germination Record**:
       - Item status is set to `Prop: Success`.
       - Date is set to the germination date recorded on the accession card.
       - Propagule type is set to seedling.
       - "Germination date." is added to the Materials: Comments section.
       - This entry is then saved.
    2. **Pricking-Out Record**:
       - Status is set to `Prop: Observed`.
       - Date is set to the pricking-out date (or ignored if pricking-out date == current date as it will update automatically).
       - Propagation: Treatment is set to ‘Transplant’.
       - Environment and Duration fields are cleared of information.
       - Medium & Container data are updated to the appropriate types and sizes.
       - Label-type-1 is set to NSTD (Nursery Standard Tag) with the request number of labels and 'NotOk' set as the label status.
       - Material: Comments are overwritten with the number of requested plants in the form (#RQ).

## Transplanting

- **Procedure**:
  - Subsequent work on the accession material follows the same workflow from the point of view of the nursery.
  - When potting up material, the accession card is removed from the germination file and annotated with the changes (mostly date, Medium & Container size), and then returned to the 'Germinated' card file.

- **IrisBG Data Entry**:
  - All post-pricking-out entries at the nursery are assigned `Prop: Observed` with the date set to the date of the work.
  - Changes are made to the Propagation: Medium and Propagation: Container values.

## Inventory

- **Procedure**:
  - Typically, the nursery is inventoried twice a year.
  - The location code (e.g., nursery is 8) is used to query all active records for the site and output this to a printable Excel file.
  - The Excel file is used as a checklist for the inventory.
  - Accession cards for accessions no longer at the nursery are removed from the ‘Germinated’ card file and moved to the ‘Historical Propagation’ card file.

- **IrisBG Data Entry**:
  - Accessions that show up as location (8) on the Excel file but are not physically found during inventory are moved to `Prop: Not Found` to indicate a lost accession (or an error on the part of a curator).
  - Otherwise, the items' status is kept as `Prop: Observed`, the date updated, and the number of specimens (No. sp.) adjusted (if changed since the last inventory).

## Death

- **Procedure**:
  - Dealing with living material means that some or entire accessions can die in cultivation at the nursery.

- **IrisBG Data Entry**:
  - If one or a few individuals die in an accession, the No. sp. is updated during the nursery inventory.
  - If the entire accession dies, the Items' status is set to `Dead`.

## Ungerminated Seed Pots

- **Procedure**:
  - Most seed lots that have not germinated in approximately 3 years are discarded.
  - The accession card is removed from the ungerminated card file and marked ‘failed to germinate’.

- **IrisBG Data Entry**:
  - The Items' status is set to `Prop: Failed to germinate or root`.
