## Export template for RFTA Art Compilation Videos

**Prefix:**

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```



**Body:**

```
<mods>
<identifier type="local">{{cells["Video Identifier"].value}}</identifier>

<titleInfo><title>{{cells['Video Title'].value}}</title></titleInfo>

{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}

{{if(isBlank(cells['Video Editor'].value), '', '<name><namePart>' + cells['Video Editor'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/edc">Editor of compilation</roleTerm></role></name>')}}

{{if(isBlank(cells['Interviewee'].value), '', '<name><namePart>' + cells['Interviewee'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ive">Interviewee</roleTerm></role></name>')}}
{{if(isBlank(cells['Interviewee2'].value), '', '<name><namePart>' + cells['Interviewee2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ive">Interviewee</roleTerm></role></name>')}}
{{if(isBlank(cells['Interviewee3'].value), '', '<name><namePart>' + cells['Interviewee3'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ive">Interviewee</roleTerm></role></name>')}}

<originInfo><dateCreated>{{cells['Video Date'].value}}</dateCreated><dateCreated encoding="edtf" keyDate="yes">{{cells['EDTF Video Date'].value}}</dateCreated></originInfo>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells["Video Extent"].value}}</extent></physicalDescription>

{{if(isBlank(cells['subject_topic'].value), '', '<subject' + if(isBlank(cells['subject_topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '">') + '<topic>' + cells['subject_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_topic_2'].value), '', '<subject' + if(isBlank(cells['subject_topic_2_URI'].value), '>', ' authority="tgm" valueURI="' + cells['subject_topic_2_URI'].value + '">') + '<topic>' + cells['subject_topic_2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_topic_3'].value), '', '<subject' + if(isBlank(cells['subject_topic_3_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject_topic_3_URI'].value + '">') + '<topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}

<typeOfResource>moving image</typeOfResource>

{{if(isBlank(cells['language'].value), '', '<language><languageTerm type="text" authority="iso639-2b">' + cells['language'].value + '</languageTerm></language>')}}
{{if(isBlank(cells['language2'].value), '', '<language><languageTerm type="text" authority="iso639-2b">' + cells['language2'].value + '</languageTerm></language>')}}

<relatedItem displayLabel="Project" type="host"><titleInfo><title>Rising from the Ashes: The Chimney Tops 2 Wildfires in Memory and Art</title></titleInfo></relatedItem>

<relatedItem type="constituent"><identifier type="pid">{{cells['Art PID'].value}}</identifier></relatedItem>

<relatedItem type="constituent"><identifier type="pid">{{cells['Related Interview file'].value}}</identifier><location><url>{{cells['Interview_Link'].value}}</url></location></relatedItem>

{{if(isBlank(cells['Related Interview file 2'].value), '', '<relatedItem type="constituent"><identifier type="pid">' + cells['Related Interview file 2'].value + '</identifier><location><url>' + cells['Interview_Link_2'].value + '</url></location></relatedItem>')}}

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>
```



**Suffix:**

```
</modsCollection>
```

