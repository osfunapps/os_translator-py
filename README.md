Introduction
------------

Run this module to translate a string to a given language using Google Translate API.

## Installation
Install via pip:

    pip install --upgrade google-cloud-translate
    pip install os-translator
    
## Usage       
    
    import os_translator.Translator as translator
    
    heb_str = translator.translate_text("What's the time?",
                                        "/path/to/service/account/.json",
                                        "firebaseprojectName",
                                        "en-US",
                                        "iw")
                                        
## Method Signatures

    def translate_text(text,
                       service_account_json_path,
                       project_id,
                       language_initials_dest,
                       language_initials_src='en-US'
                       ):
        """Will translate a text to a given language
    
        Parameters:
        :param text: the text to translate
        :param service_account_json_path: the path to your google translate api json key. Download from your firebase's project's settings
        :param project_id: your project id (fetch from your api console project's name: https://console.cloud.google.com/?_ga=2.55756075.1423406147.1582784765-1154152733.1582784765)
        :param language_initials_dest: the initials of the language you want to translate to
        :param language_initials_src: the source language
    
        NOTICE:
            If there are substrings you don't want to translate, write KEEP before them. Example: "The boy looks KEEPWord"
        """

## Licence
MIT