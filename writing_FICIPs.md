# FICIPs 
Filecash Improvement Proposals (FICIPs) describe standards for the Filecash platform, including core protocol specifications, client APIs, and other changes to the project.

# Contributing

 1. Review FICIP-1.
 2. Fork the repository by clicking "Fork" in the top right.
 3. Add your FICIP to your fork of the repository. There are [template FICIPs here](/templates).
 4. Submit a Pull Request to Filecash's [FICIPs repository](https://github.com/filecash/FICIPs).
 5. Draft and submit a Pull Request to the [Filecash Specification repository](https://spec.file.cash) to update the spec with the changes that your FICIP brings.

Your first PR should be a first draft of the final FICIP. It must meet the formatting criteria enforced by the build (largely, correct metadata in the header). An editor will manually review the first PR for a new FICIP and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to a discussion forum or open GitHub issue where people can discuss the FICIP as a whole.

If your FICIP requires images, the image files should be included in a subdirectory of the `assets` folder for that FICIP as follow: `assets/ficip-X` (for ficip **X**). When linking to an image in the FICIP, use relative links such as `../assets/ficip-X/image.png`.

Once your first PR is merged, we have a bot that helps out by automatically merging PRs to draft FICIPs. For this to work, it has to be able to tell that you own the draft being edited. Make sure that the 'author' line of your FICIP contains either your Github username or your email address inside `<triangular brackets>`. If you use your email address, that address must be the one publicly shown on [your GitHub profile](https://github.com/settings/profile).

When you believe your FICIP is mature and ready to progress past the draft phase, you should do one of two things:

 - **For a Standards Track FICIP of type Core**:
 	- ask to have your issue added to the agenda of an upcoming All Core Devs meeting, where it can be discussed for inclusion in a future chain upgrade. If implementers agree to include it, the FICIP editors will update the state of your FICIP to 'Accepted'.
 	- prepare the changes to the spec text necessary to describe the protocol modifications that your FICIP brings. Submit a PR to the [Filecash Specification repository](https://spec.file.cash). These changes will also be discussed in the "All Core Devs" meeting and the editor will assign a reviewer.
 - **For all other FICIPs**, open a PR changing the state of your FICIP to 'Final'. An editor will review your draft and ask if anyone objects to its being finalised. If the editor decides there is no rough consensus - for instance, because contributors point out significant issues with the FICIP - they may close the PR and request that you fix the issues in the draft before trying again.

# FICIP Status Terms
* **Draft** - a FICIP that is undergoing rapid iteration and changes.
* **Last Call** - a FICIP that is done with its initial iteration and ready for review by a wide audience.
* **Accepted** - a core FICIP that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author. The process for Core Devs to decide whether to encode a FICIP into their clients as part of a hard fork is not part of the FICIP process. If such a decision is made, the FICIP wil move to final.
* **Final (non-Core)** - a FICIP that has been in Last Call for at least 2 weeks and any technical changes that were requested have been addressed by the author.
* **Final (Core)** - a FICIP that the Core Devs have decided to implement and release in a future chain upgrade or has already been released in a chain upgrade. 
* **Deferred** - a FICIP that is not being considered for immediate adoption. May be reconsidered in the future for a subsequent chain upgrade.

# Preferred Citation Format

TODO: 
The canonical URL for a FICIP that has achieved draft status at any point will be on the Filecash website. For example, the canonical URL for FICIP-00001 will be https://file.cash
