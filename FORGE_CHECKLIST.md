# Forge submission checklist

This checklist maps the repository to the official Hack Club Forge requirements. It does not replace Forge's review or the builder's own journal and proof.

Official references: [submission requirements](https://forge.hackclub.com/docs/requirements/submitting), [project guidelines](https://forge.hackclub.com/docs/requirements/project-guidelines), [JOURNAL.md format](https://forge.hackclub.com/docs/design/journal-format), and [pitching](https://forge.hackclub.com/docs/requirements/pitching).

## Present in this repository

- README explaining what Starbie is, what it does, why it was created, how to assemble it, and how to use it
- Full populated-board render plus front and back PCB renders
- BOM in CSV format with quantities, prices, purchase links, vendors, purposes, and a total-cost line
- KiCad schematic, PCB, project, custom symbols, and footprints
- Gerber and drill fabrication files plus the ready-to-upload Gerber ZIP
- Arduino source firmware and setup instructions
- Populated-board GLB, Blender render source, and the available component STEP models
- Original design walkthrough, library care package, and reference images
- Source attribution and license

## Builder action still required

- **Originality:** Forge requires an original design made by the submitter. This repository identifies the design as imported from SharKingStudios/Starbie and credits Logan Peterson. Only submit it if you are the designer or can accurately document your own distinct contribution.
- **Complete mechanical CAD:** Add a full-assembly STEP export and any enclosure or mounting design required to make the finished project solid. The repository currently has a populated-board GLB, Blender source, and component STEP files, but not one full project STEP assembly.
- **Attachment review:** Confirm every physical component has a concrete mounting method and document any enclosure, screws, clips, or other hardware that the final build needs.
- **Sanity check:** Ask another person to review the PCB, firmware, BOM, and mechanical assembly. Fix the issues they find before submitting.
- **Journal:** Replace or supplement the Half Life mirror with authentic entries written in your own words. Each Forge Git journal entry needs a `# Date: Title` heading, at least one progress image, and `**Total time spent: X hours**`. Explain what you did, why you did it, and any problems or failures. Forge says AI-generated journal content will be rejected.
- **Physical build submission:** Add progress photos to the journal, finished-build photos to the README, and a demo-video link. Lapse the build phase when possible and update the design files for any physical rework.
- **Eligibility and account steps:** Forge is for Hack Club Slack members ages 13–18. Create the project on Forge, verify your identity through Hack Club Auth, and add your shipping address in settings.
- **Forge project fields:** Link this repository, add a short project description, upload a cover image, and add at least one devlog entry. `Renders/Starbie Render.png` is the strongest existing cover-image candidate.
- **AI disclosure:** Forge's project form asks builders to declare when AI contributed more than roughly 20% of a project and describe that use. Answer this accurately for your work.
- **Pitch if Tier 1:** A Slack pitch in `#forgery` is required only for Tier 1. It must include the idea, what you are designing, references, past work, why it merits more than $200, and a rough BOM with a total.

## Current BOM total

The current estimated component cost is **$24.73 before shipping and taxes**. Confirm live prices and shipping before requesting funding.
