# AI-Helper Annotation Privacy Policy

**Last updated:** October 21, 2026

**Developer:** Vitaliy Panchenko  
**Contact:** vitpan2010@gmail.com  
**Support page:** https://github.com/FIOWB21/ai-annotator/issues/1

## Purpose of the Extension

AI-Helper for annotation reads text selected by the user on permitted Argilla pages, sends it to the AI provider selected by the user, and displays the automated annotation result in the browser.

The extension does not process text without user action, except when the user has enabled automatic mode.

## What Data Is Processed

### Webpage Text

When processing is started, the extension extracts text from page elements selected by the user. This text, along with the prompt and system instruction selected by the user, is sent to the AI service chosen in the extension settings.

Built-in supported services include Groq, Google Gemini, Cerebras, Mistral, OpenRouter, and DeepSeek. The user may also specify their own OpenAI-compatible HTTPS API.

The AI response is shown to the user in the extension. The extension developer does not receive this text directly.

### Settings and Keys

The following are stored in Chrome's local storage:

- AI provider settings and their API keys;
- user-created prompts;
- interface and keyboard shortcut settings;
- the list of websites to which the user has granted access;
- shared prompt library settings, including the username and access code if the user uses this feature;
- a random installation identifier required for the shared prompt library to work.

This data is used to operate the extension and is not sent to the developer on its own. API keys are sent only to the relevant AI service when processing a user request.

### Shared Prompt Library and Supabase

If the user connects to the shared prompt library, requests are sent to a Supabase Edge Function in the developer's project.

Depending on the action performed, Supabase may receive:

- a random installation identifier;
- the name provided by the user for publications;
- an access code used to verify access rights;
- the prompt title and text when manually publishing a prompt;
- the prompt identifier and title when adding a prompt to the local library;
- the technical events `active` and `prompt_added` for aggregated statistics.

The access code is used to verify the user's role and is not stored in statistics tables. Webpage text and AI provider API keys are not sent to Supabase.

## Purposes of Processing

Data is used only to:

1. perform automated text annotation;
2. save user settings and prompts;
3. operate the shared prompt library;
4. maintain and measure the operation of the shared library.

Data is not used for advertising, profiling, sale, marketing, or tracking browsing history.

## Sharing Data with Third Parties

Page text is sent only to the AI provider selected by the user, as this is necessary to obtain the annotation result.

Shared library data is sent to Supabase as necessary to publish, download, and delete shared prompts.

The use of data by AI providers and Supabase is governed by their own privacy policies. Users should review the terms of the service they select.

The developer does not sell user data, use it for personalized advertising, or make it available for people to read, except where required by law or necessary for service security.

## Storage and Deletion

Local data is stored in the Chrome profile until the user clears the extension's data in Chrome settings or removes the extension.

Published prompts remain in the shared library until they are deleted by a user authorized to delete them or by the project administrator.

Technical events from the shared library are stored in Supabase for usage statistics. Users may contact the developer at the address above to request deletion of data associated with them. The request may require verification that the data belongs to the requester.

## Security

Data is transmitted between the extension and remote services over HTTPS. The extension does not request or process website passwords, cookies, browser history, bank card details, or location coordinates.

Users are responsible for keeping their API keys and access codes secure and should not share them with others.

## Limited Use of Data

The use of data collected by the extension is limited to providing and improving its single purpose: automated annotation of text selected by the user and related shared prompt library features. Data is not used for advertising, sale, profiling, or unrelated purposes.

## Policy Changes

If data processing practices change, this policy will be updated before the corresponding extension version is released. The last updated date is shown at the beginning of this document.

## Contact

For questions about privacy, data deletion, or the extension, contact: vitpan2010@gmail.com.
