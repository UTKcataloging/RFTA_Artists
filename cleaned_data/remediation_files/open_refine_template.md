# Open Refine Template for RFTA Artists Collection


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["identifier"].value}}</identifier>
<identifier type="pid">{{cells["PID"].value}}</identifier>
{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}} 
{{if(isBlank(cells['dateIssued'].value), '', '<originInfo><dateIssued>' + cells['dateIssued'].value + '</dateIssued><dateIssued encoding="edtf" keyDate="yes">' + cells['dateIssued'].value + '</dateIssued><publisher>' + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place></originInfo>')}}
<abstract>{{cells["abstract"].value}}</abstract>
<name{{if(isBlank(cells["artist_URI"].value), '', ' authority="naf" valueURI="' + cells["artist_URI"].value + '"')}}><namePart>{{cells["artist"].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/art">Artist</roleTerm></role></name>
{{if(isBlank(cells["interviewee_1"].value), '', '<name>' + '<namePart>' + cells["interviewee_1"].value + '</namePart>' + '<role>' + '<roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ive">Interviewee</roleTerm>' + '</role>' + '</name>')}}
{{if(isBlank(cells["interviewee_2"].value), '', '<name>' + '<namePart>' + cells["interviewee_2"].value + '</namePart>' + '<role>' + '<roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ive">Interviewee</roleTerm>' + '</role>' + '</name>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form></physicalDescription> 
{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_2_URI'].value + '"><topic>' + cells['subject_topic_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_3_URI'].value + '"><topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_4_URI'].value + '"><topic>' + cells['subject_topic_4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_5'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_5_URI'].value + '"><topic>' + cells['subject_topic_5'].value + '</topic></subject>')}}
<typeOfResource>text</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Rising from the Ashes: The Chimney Tops 2 Wildfires in Memory and Art.</title></titleInfo></relatedItem>
{{if(isBlank(cells["interview_file"].value), '', '<relatedItem type="references">' + '<location>' + '<url>' + cells["interview_link"].value + '</url>' + '</location>' + '<identifier type="pid">' + cells["interview_file"].value + '</identifier>' +'</relatedItem>')}}
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```