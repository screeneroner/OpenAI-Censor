# OpenAI Censor

## Three can keep a secret if two are dead

AI is a powerful tool that may use your inputs to "improve models," "enhance your experience," and other similar purposes. This means YOUR TEXTS MUST BE STORED SOMEWHERE, in a location that you do not have access to verify or delete them. Even if you accidentally send your ABSOLUTELY PRIVATE information, it could be stored. To prevent even a theoretical possibility of disclosing your own secrets or confidential information about clients and/or customers, you SHOULD NOT SHARE IT AT ALL! However, for example, if you are using AI to correct grammar, wording, and tone of your letters, you must use the exact text in the AI prompts.

## Hide it to keep it

The solution for this dichotomy is straightforward—just replace real words with their 'anonymized' analogs! Instead of calling your client by its real name 'Super Secret IT Company LTD.', use 'Client Company Name' in the prompt. There are two main problems with this approach. The first is that there may be many places in your text where you need to make these changes. It can take a lot of time to replace them all, and you may miss some entries, leaving them unhidden. The second problem is that the response from the AI will contain these 'anonymized' words, and you will need to replace them back to get 'unhidden' text.

This script will handle the above-described routine for you! You should prepare the encrypting file in a zebra-like format. The first row contains the real word(s), and the second row contains its anonymized version. Like this:
```
Apple
Client Company
Steve Jobs
John Smith
```
The script will inject the transcoding codes into the OpenAI ChatGPT web page along with three buttons below the entry field: Choose File, Unhide, and Hide. The first button will load the 'encrypting' file (you may use several ones). When you press the Hide button, it will scan the entire page (including the prompt entry text area) and replace real words with anonymized ones. From this moment, you can safely send your texts to the AI. Once you get a response and press the Unhide button, the script will do a reverse translation, and you will see the original texts and words ready to be copy-pasted. 

The important point here is that the AI operates with anonymized text only. The real, de-anonymized texts remain in the operational memory of your local computer and become unhidden only when you load the proper encoding file and press the Unhide button!

## How to use this script

1. Download and install a browser add-on like Tampermonkey (or similar)
2. Install this OpenAI Censor script according to the add-on's script installation procedure.
3. Prepare and save the encoding file with pairs of rows that contain real and encoded text.
4. Open the ChatGPT web page. You should see a new row with the script buttons under the input area.
5. Press the Choose File button and load your encryption file.
6. Type your prompt.
7. Press the Hide button and verify that all real words were anonymized.
8. Send the anonymized prompt to the AI and get its response.
9. Press the Unhide button to replace anonymized words with the originals and get the original texts.
10. Profit!

# Example

### Encoding file
```
Apple
Client Company
Steve Jobs
John Smith
Steve
John
Berkshire Hathaway
Finance Parnter
Warren Buffett
Financier
```

### Original message
> Hi __Steve__,
> 
> I wanted to share an exciting opportunity for __Apple__ to partner with __Berkshire Hathaway__. Given Warren __Buffett's__ reputation for strategic investments and __Apple's__ innovative technology, this collaboration with __Warren Buffett__ could be groundbreaking. Let's explore how __Apple__ and __Berkshire Hathaway__ can create a powerful synergy.
> 
> Best,
> __Joe__

### Encrypted message
> Hi __John__,
> 
> I wanted to share an exciting opportunity for __««Client Company»»__ to partner with __««Finance Parnter»»__. Given __««Financier»»'s__ reputation for strategic investments and __««Client Company»»'s__ innovative technology, this collaboration with __««Financier»»__ could be groundbreaking. Let's explore how __««Client Company»»__ and __««Finance Parnter»»__ can create a powerful synergy.
> 
> Best,
> __Joe__
