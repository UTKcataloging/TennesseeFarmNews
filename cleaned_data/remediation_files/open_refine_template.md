# Open Refine Template for Tennessee Farm News


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["adminDB"].value}}</identifier>
<identifier type="pid">{{cells['PID'].value}}</identifier>
<titleInfo><title>{{cells["title"].value}}</title></titleInfo> 
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
<physicalDescription><form authority="aat">{{cells['form'].value}}</form>{{if(isBlank(cells['extent'].value), '', '<extent>' + cells['extent'].value + '</extent>')}}</physicalDescription>
{{if(isBlank(cells['date_year'].value), '', '<originInfo><dateIssued>' + cells['date_year'].value + '</dateIssued><publisher>' + cells['publisher'].value + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place><issuance>serial</issuance></originInfo>')}}
<note>{{cells['note'].value}}</note>
{{if(isBlank(cells['subject1'].value), '', '<subject authority="lcsh"><topic>' + cells['subject1'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh"><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh"><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject5'].value), '', '<subject authority="lcsh"><topic>' + cells['subject5'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject6'].value), '', '<subject authority="lcsh"><topic>' + cells['subject6'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject7'].value), '', '<subject authority="lcsh"><topic>' + cells['subject7'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject authority="naf"><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
<subject authority="naf" valueURI="http://id.loc.gov/authorities/names/n79060965"><geographic>Tennessee</geographic><cartographics><coordinates>35.75035, -86.25027</coordinates></cartographics></subject>
<classification authority="lcc">{{cells['classification'].value}}</classification>
<typeOfResource>{{cells['item_type'].value}}</typeOfResource>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
</mods>

```

#### Suffix

```
</modsCollection>
```