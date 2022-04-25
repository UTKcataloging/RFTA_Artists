## Export template for RFTA Art Compilation Videos

**Prefix:**

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```



**Body:**

```
<mods>
<identifier type="local">{{cells["identifier"].value}}</identifier>

<titleInfo><title>{{cells['title'].value}}</title></titleInfo>

{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}

<originInfo><dateIssued encoding="edtf" keyDate="yes">{{cells['date_text'].value}}</dateIssued></originInfo>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells["extent"].value}}</extent></physicalDescription>

{{if(isBlank(cells['subject_name'].value), '', '<subject'+ if(isBlank(cells['subject_name_URI'].value), '', ' valueURI="' + cells['subject_name_URI'].value + '"' + ' authority="wikidata"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}

<subject authority="naf" valueURI="http://id.loc.gov/authorities/names/n90646627"><name><namePart>Tennessee Volunteers (Football team)</namePart></name></subject>

{{if(isBlank(cells['subject_name_3'].value), '', '<subject'+ if(isBlank(cells['subject_name_3_URI'].value), '', ' valueURI="' + cells['subject_name_3_URI'].value + '"' + ' authority="wikidata"') + '><name><namePart>' + cells['subject_name_3'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_name_4'].value), '', '<subject'+ if(isBlank(cells['subject_name_4_URI'].value), '', ' valueURI="' + cells['subject_name_4_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject_name_4'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_topic'].value), '', '<subject' + if(isBlank(cells['subject_topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '">') + '<topic>' + cells['subject_topic'].value + '</topic></subject>')}}

<subject><topic>{{cells['subject_topic_2'].value}}</topic></subject>

{{if(isBlank(cells['subject_topic_3'].value), '', '<subject' + if(isBlank(cells['subject_topic_3_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject_topic_3_URI'].value + '">') + '<topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}

<typeOfResource>text</typeOfResource>

<relatedItem displayLabel="Project" type="host"><titleInfo><title>University of Tennessee Volunteers Football Media Guides</title></titleInfo></relatedItem>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>
```



**Suffix:**

```
</modsCollection>
```

