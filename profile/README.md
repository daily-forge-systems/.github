<div align="center">

# Quorvyn

_Desktop applications for work where the material itself is the sensitive part_

[Website](https://quorvyn.de) · [Products](https://quorvyn.de/produkte/) · [About](https://quorvyn.de/ueber/) · [Security](https://quorvyn.de/sicherheit/) · [Contact](https://quorvyn.de/kontakt/)

</div>

Quorvyn builds desktop applications in Berlin for Windows and Linux. They are made for material that nobody uploads casually, such as your own documents, your own training data and your own measurement series. This organisation, `daily-forge-systems`, holds the source code of those applications and the shared toolkit they are built on. The website at [quorvyn.de](https://quorvyn.de) is in German for now, and its [imprint](https://quorvyn.de/rechtliches/impressum/) states who stands behind Quorvyn.

## Why the applications run on your machine

The usual route for sensitive material is to upload it, have it analysed in the cloud and get a result back. That asks for trust exactly where the least trust is available, and it leaves a copy of every job in a place you do not control. Quorvyn turns this around. Where an application can do its work on your own machine, it does, and the analysis models ship with the application and run there. An upload path that does not exist cannot be switched on by accident.

This costs something. Local processing is more work to build than the cloud route, and it rules some features out. It also replaces neither encryption on the device nor traceable updates, and where an application only gives pointers rather than findings, its product page says so.

## What we are building

None of the applications can be obtained yet. Each product page on the website states whether it is in development or still a concept, together with the planned platforms.

| Application | What it does | Status |
| --- | --- | --- |
| [Docyra](https://quorvyn.de/produkte/docyra/) | Turns photos and scans into ordered documents. It finds the edges, straightens the page, reads the text and files it searchably, with the archive encrypted on your disk. | In development |
| [GuideFlow](https://quorvyn.de/produkte/guideflow/) | Takes you in eight steps from a folder of pictures to a checked image model, without the machine learning vocabulary. Training and evaluation run on your own machine. | In development |
| [Prismio](https://quorvyn.de/produkte/prismio/) | Evaluates metallographic micrographs, component photographs and CT volumes in one application and keeps every step from the raw data to the released report traceable. | Concept |

## How we work

The applications are written in Flutter and share a common set of Dart packages for the parts that are not specific to one product. Model training is built in Python, and the website is a static Astro site that ships no client-side JavaScript.

Every product repository keeps its privacy, AI and security records next to its code, in the same change as the code they describe. A question that only a person can answer, such as a legal basis or a risk classification, stays open in those records and blocks the release until someone has answered it. Every repository is also scanned for leaked secrets and checked with static analysis.

## Why the code is private

The product repositories are private, so there is nothing here to clone, install or contribute to. This `.github` repository is the only public one. It carries this page and the defaults for issues and pull requests that the organisation's repositories share. Once an application is released, it will be available through the website.

## Contact

| Topic | Where |
| --- | --- |
| General questions and press | [contact@quorvyn.de](mailto:contact@quorvyn.de) or the [contact page](https://quorvyn.de/kontakt/) |
| Using or setting up an application | [support@quorvyn.de](mailto:support@quorvyn.de) |
| Security vulnerabilities | [security@quorvyn.de](mailto:security@quorvyn.de), confidentially and never as a public issue. The [security page](https://quorvyn.de/sicherheit/) and [security.txt](https://quorvyn.de/.well-known/security.txt) describe the process. |
