# People Section User Guide

The people page ([`_pages/people.md`](_pages/people.md)) is a photo grid: each member is
one card with a square photo, name, position, and social icons. Everything lives in the
page's YAML front matter — there are no per-person Markdown files any more.

- Layout: [`_layouts/profiles.html`](_layouts/profiles.html)
- Styles: [`_sass/_people.scss`](_sass/_people.scss)
- Social icons: [`_includes/social_profile.html`](_includes/social_profile.html)

## How to Add a New Member

### 1. Add an entry to the `profiles` list in `_pages/people.md`

```yaml
profiles:
  - role: PhD                              # which section the card goes in (see `groups`)
    name: Jane Doe                         # displayed name
    image: people/janedoe.jpg              # path relative to assets/img/
    position: PhD Student                  # position line; <br> is allowed
    image_position: center 25%             # optional, see "Photo framing" below
    image_circular: false                  # optional, true = round avatar
    social:                                # all fields optional
      email: jane.doe@mbzuai.ac.ae
      website: https://janedoe.github.io/
      scholar_userid: GOOGLE_SCHOLAR_ID
      github_username: github_username
      linkedin_username: linkedin-username
      twitter_username: twitter_handle
      orcid_id: 0000-0000-0000-0000
      research_gate_profile: ResearchGate_Name
```

If `social.website` is set, the name itself also links to it.

### 2. Add the photo

Put it in [`assets/img/people/`](assets/img/people/). Photos are cropped to a square
(`object-fit: cover`), so a roughly square, face-centred image works best.
Recommended: 400x400 px, under 500 KB.

### 3. Check the framing

The square crop is taken from the centre by default, which clips the top of the head on
tall portraits. If that happens, set `image_position` on the profile — it maps straight
to CSS `object-position`, where the second value is how far down the crop window sits:

| Value | Effect |
| --- | --- |
| `center 0%` / `center top` | crop from the top — use when the head is clipped |
| `center 50%` | the default |
| `center 100%` / `center bottom` | crop from the bottom — use for full-body shots |

Panning only moves the window; it cannot zoom in. If the person is small in the frame
(distant or scenic shots), the only fix is a tighter source photo.

## Sections

Sections and their order come from the `groups` list in the front matter. Each group
pulls every profile whose `role` matches:

```yaml
groups:
  - title: Faculty
    role: PI
  - title: PhD Students
    role: PhD
    note: Optional small grey line under the heading.
```

Current roles: `PI`, `Postdoc`, `PhD`, `MSc`, `Visiting`. To add a section, add a
`groups` entry with a new `role` and use that `role` on the relevant profiles. A group
with no matching members is skipped, so you can leave it in place.

Within a section, cards appear in the order the profiles are listed. The grid fits four
cards per row on desktop and two on mobile.

## Alumni

Alumni live in the Markdown body of `_pages/people.md`, below the front matter, as plain
Markdown tables (name / degree / period). They render as compact rows on desktop and
stack into blocks on mobile.

## Removing Someone Temporarily

Comment out their `profiles` entry with `#`, as done for past visiting students.
