# Open Refine Template for RFTA Artists Collection - Compound Objects


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="pid">{{cells["PID"].value}}</identifier>
{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}} 
{{if(isBlank(cells['dateIssued'].value), '', '<originInfo><dateCreated>' + cells['dateIssued'].value + '</dateCreated>' + if(isBlank(cells['dateIssued_start'].value), '<dateCreated>' + cells['dateIssued'].value + '</dateCreated>', '<dateCreated encoding="edtf" point="start">' + cells['dateIssued_start'].value + '</dateCreated><dateCreated encoding="edtf" point="end">' + cells['dateIssued_end'].value + '</dateCreated>') + '</originInfo>')}}
<abstract>{{cells["abstract"].value}}</abstract>
<name{{if(isBlank(cells["artist_URI"].value), '', ' authority="naf" valueURI="' + cells["artist_URI"].value + '"')}}><namePart>{{cells["artist"].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/art">Artist</roleTerm></role></name>
{{if(isBlank(cells["interviewee_1"].value), '', '<subject>' + '<name>' + '<namePart>' + cells["interviewee_1"].value + '</namePart>' + '</name>' + '</subject>')}}
{{if(isBlank(cells["interviewee_2"].value), '', '<subject>' + '<name>' + '<namePart>' + cells["interviewee_2"].value + '</namePart>' + '</name>' + '</subject>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><form authority="aat" valueURI="http://vocab.getty.edu/aat/300136900">motion pictures (visual works)</form></physicalDescription> 
{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_2'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_2_URI'].value + '"><topic>' + cells['subject_topic_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_3'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_3_URI'].value + '"><topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_4'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_4_URI'].value + '"><topic>' + cells['subject_topic_4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_5'].value), '', '<subject authority="tgm" valueURI="' + cells['subject_topic_5_URI'].value + '"><topic>' + cells['subject_topic_5'].value + '</topic></subject>')}}
<typeOfResource>still image</typeOfResource>
<typeOfResource>moving image</typeOfResource>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Rising from the Ashes: The Chimney Tops 2 Wildfires in Memory and Art</title></titleInfo></relatedItem>
{{if(isBlank(cells["interview_file"].value), '', '<relatedItem type="references">' + '<location>' + '<url>' + cells["interview_link"].value + '</url>' + '</location>' + '<identifier type="pid">' + cells["interview_file"].value + '</identifier>' +'</relatedItem>')}}
{{if(isBlank(cells["PID_art"].value), '', '<relatedItem type="constituent" displayLabel="art">' + '<identifier type="pid">' + cells["PID_art"].value + '</identifier>' + '<identifier type="local">' + cells["identifier"].value + '</identifier>' + '</relatedItem>')}}
{{if(isBlank(cells["PID_video"].value), '', '<relatedItem type="constituent" displayLabel="compilation video">' + '<identifier type="pid">' + cells["PID_video"].value + '</identifier>' + '<identifier type="local">' + cells["identifier_video"].value + '</identifier>' + '</relatedItem>')}}
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```