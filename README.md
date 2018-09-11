# Editor JSON File Specifications

The file must contain a JSON Object with some mandatory fields:

## Version

The field is called ```editorVersion``` and must be an integer , superior to zero. It is used to determine if there is a change in the file when loading it in the Fidzup CMP.

example:

```json
{
  "editorVersion": 5,

  ...

}
```

## Date of last modficiation

It contains exactly what it's name (```lastUpdated```) means... The date of the last modficiation of the file (or the date of the last version).

example:

```json
{
  "editorVersion": 5,
  "lastUpdated": "2018-07-23T15:03:22Z",

  ...

}
```

## Integer identifier

An integer identifying the editor itself called ```id```. This id is not used internaly in the Fidzup CMP. But it's used in some editor's internal system, to tag some applications. It must be a positive integer.

example:

```json
{
  "editorVersion": 5,
  "lastUpdated": "2018-07-23T15:03:22Z",
  "id": 9,

  ...

}
```

## Name

It's a string which can be displayed on the Fidzup CMP. It's called ```name```.

exmaple:

```json
{
  "editorVersion": 5,
  "lastUpdated": "2018-07-23T15:03:22Z",
  "id": 9,
  "name": "My Editor Name",

  ...

}
```

## Privacy policy URL

```policyURL```, is the link to your website, on the page where stands the privacy policy of your company.

example:

```json
{

  ...

  "policyUrl": "https://www.example.com/privacy-policy/",

  ...

}
```

## Purposes

Here is an array of ```purposes```. The format is eaxctly the same as the IAB purpose definition. each purpose must contain an ```id```, a ```name``` and a ```description```.

example:

```json
{

  ...

  "purposes": [
    {
      "id": 1,
      "name": "Storage and access of information",
      "description" : "The storage of information, or access to information that is already stored, on your device such as accessing advertising identifiers and/or other device identifiers, and/or using cookies or similar technologies."
    }
  ],

  ...

}
```

## Features

Here is an array of ```features```. The format is eaxctly the same as the IAB feature definition. Each feature must contain an ```id```, a ```name``` and a ```description```.

example:

```json
{

  ...

  "features": [
    {
      "id": 1,
      "name": "Matching Data to Offline Sources",
      "description" : "Combining data from offline sources that were initially collected in other contexts."
    }
  ]
}
```

# Localization

To have your file translated in multiple language, it's simple. You just have to provide with the language in it's name under the format editor-{language}.json. Where language is the language code following the Two-letter ISO639-1 format.
