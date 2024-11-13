---
slug: how-to-implement-sso-in-docebo-for-seamless-user-experience
title: How to Implement SSO in Docebo for Seamless User Experience
authors: [undirected]
---


# How to Implement SSO in Docebo for Seamless User Experience

There was this time, deep in the catacombs of a Monday morning meeting, where we were grappling with the endless battle of passwords. You know the drill—half the squad mysteriously forgetting theirs just moments before they needed them. It was during one of these existential chats, over an embarrassingly cold cup of coffee, that the idea of implementing SSO (Single Sign-On) in our Docebo platform was born. It seemed like the Holy Grail for our bedraggled team of learners and managers. Our shared brain trust decided it was time to marry convenience with technology to usher in an era of seamless user experience. Oh, what hope we had.

## Discovering the Magic of SSO

Backstage, while the world continued without us for a few hours, we set forth to navigate the tangled web of technical set-ups. Implementing SSO isn't just about typing in some arcane code and expecting silver linings; it's a ritualistic dance that uncovers a smoother path for users who can't be bothered with passwords. Why not empower them to bypass the gates with ease?

First things first, we needed to determine precisely which SSO method we desired to flirt with. Between SAML and OAuth2, we cuddled up with SAML—it was like picking your starter Pokémon, and we were great with Charizard. So here we go, each step like placing careful footfalls on a soggy forest floor.

### Step One: Understanding SAML

SSO via SAML (Security Assertion Markup Language) seemed like an ancient scroll written in digital ink. It basically allows identity providers to pass authorization credentials to service providers, which is just a fancy way to say: users can hop from app to app like merry travelers, without disruption. Think of it as a backstage pass to the concert of your favorite digital services.

Our first task was to understand how the heck to configure this ancient text of magnificence within Docebo. Under Admin Menu, there's a settings option bravely waiting for our click. With anticipation, we navigated to Advanced Settings, like explorers opening a mystical door.

### Step Two: Gather the Necessary Ingredients

SSO implementation is a bit like making the perfect cup of tea. Gather your elements wisely:

- **Identity Provider's SAML Metadata**: It's like your grandma's secret recipe card—something of a treasure. Usually provided by whoever manages your identity setup.
- **Docebo's SSO Service Provider Settings**: A unique bundle, found right in your Docebo portal. We found this under the menus we traipsed through, it felt like unearthing a relic.

With these primary ingredients at hand, we brewed up a concoction that even Gandalf would approve of.

### Step Three: Configure Identity Provider

This is where magic meets reality, one configuration at a time. We tinker with our identity provider—be it Okta, OneLogin, or a dash of Azure AD. Without getting lost in the scuffle, here’s the gist:

1. **Upload the relevant metadata** from Docebo into the Identity Provider (IdP). Easy peasy.
2. **Create a SAML application** and pour in the data, matching the Docebo endpoints like yin and yang.

While Suzanne, from our IT department, cobbled together her side of the IdP, we made "ooh" faces at how everything started meshing like gears undone from a machine long ago.

### Step Four: Configure Docebo's SSO

Now, for the big shebang—connecting Docebo to dance harmoniously with our configured IdP.

1. In Docebo's Advanced Settings, select the **SAML 2.0** tab. Secret club, right?
2. Insert your unique SAML configurations provided by the IdP. It's like getting a stamp of approval.
3. We tinkered with enabling automatic account provisioning - letting newcomers roll in without filling out the boring forms.

Doesn’t end here, though. Testing is paramount. It's like setting off fireworks to see if they impress the neighbors or badly set things ablaze.

### Step Five: Test the SSO Integration

And so, like every great quest, we tested our resolve. We clicked log in without typing a password and waited. Minutes stretched like hours. But lo and behold, it worked! Users sailed smoothly through the gateway, no cryptic codes needed. Seeing happy team faces pop up without frowns - utterly worth it.

### Final Thoughts

What a journey! Implementing SSO in Docebo felt like knitting an epic tapestry where our users moved seamlessly from one service vista to another. And while the endeavor required setting aside some dedicated hours—it mostly required patience, coffee, and the occasional chuckle at our missteps.

Let this tale inspire you: grant your team the freedom to roam unfettered through the fields of your digital landscape. As we sit around now, reminiscing over how we conquered that beast, we can't help but laugh at how something so valuable seemed daunting at first. Yet here we are, together, basking in the glow of our password-free utopia. Until the next challenge knocks on our door, let’s sip our beverages (hot, this time) and revel in the marvels we’ve achieved. Here's to seamless experiences that make our digital lives just a smidge more beautiful.