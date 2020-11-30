---
title: "Organaizing Contacts with Python"
date: 2020-10-13T20:59:16+03:00
draft: false
---
At work I come accross many people's contacts mostly of which I have to
store in my phone, create groups for further communication etc. When I am
dealing with more than 200 contacts per week, things can get messy and
tedious that is why I have found a nice way to inject some Python into 
my contacts workflow.

The workflow is as follows:

* Receive contact info in a word document.
* Lift the contact data into Ms Excel and save it as a csv file
* Convert the csv int a vcf format which handled contact info
* Merge all the many vcf files into one handy file containing many contacts
* Share with team members who just import into their contacts list.

## Tools

* Python
* [csv2vcard 0.2.2](https://pypi.org/project/csv2vcard/) 

## VCF vCard Format Introduction

vCard, also known as VCF (Virtual Contact File), is a file format standard for 
electronic business cards. vCards are often attached to e-mail messages but can be 
exchanged in other ways, such as Multimedia Messaging Service (MMS), on the World Wide Web, 
instant messaging or through QR code. They can contain name and address information, 
telephone numbers, e-mail addresses, URLs, logos, photographs, and audio clips.

## CSV and VCF

After importing the contact into into Excel, create the following columns to handle
the contact info:

* last_name
* first_name
* org
* title
* phone
* email
* website
* street
* city
* p_code
* country

These colums are quite important since python's csv2vcard requires that they be present in the CSV file.
Convert the document to a CSV file with the above columns as required. Its okay to have blank columns
if such data is not available.

## csv2vcard

The operation of csv2vcard is done in a Python environment. So execute Python

```
Python

from csv2vcard import csv2vcard
csv2vcard.csv2vcard('contacts.csv',',')
```
The code above will create a folder called export with all the many vcards inside it. This is good but we
want one single vcard, so we are going to use Linux's cat program. Go into the export folder and execute the
following code:

```
cat * >> contacts.vcf
```
The output shall be one vcf file with all the contacts.

You can now share the file and/or copy it to your phone and import into your contacts.

Enjoy :-)
