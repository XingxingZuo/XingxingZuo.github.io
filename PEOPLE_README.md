# People Section User Guide

## How to Add New Members

### 1. Edit the `_pages/people.md` File

Add new member configurations in the `profiles` section:

```yaml
profiles:
  - align: right           # Image alignment: left or right
    image: people/NAME.jpg # Image path (relative to assets/img/)
    content: NAME.md       # Member detail file (in _pages/ directory)
    image_circular: false  # Whether to display as circular avatar
    more_info: >          # Basic information (position, office, etc.)
      <p>Position</p>
      <p>Office: Room XXX</p>
    social:               # Social media links (optional)
      email: name@example.com
      website: https://personal-website.com
      scholar_userid: GOOGLE_SCHOLAR_ID
      github_username: github_username
      linkedin_username: linkedin-username
      twitter_username: twitter_handle
      orcid_id: 0000-0000-0000-0000
      research_gate_profile: ResearchGate_Name
```

### 2. Create Member Detail File

Create a `NAME.md` file in the `_pages/` directory, content example:

```markdown
## Member Name

**Research Interests:** List research interest areas

Brief personal introduction...

### Education Background
- Ph.D. in XXX, University Name, Year
- M.S. in XXX, University Name, Year
- B.S. in XXX, University Name, Year

### Research Projects (Optional)
- Project 1: Brief description
- Project 2: Brief description

### Representative Papers (Optional)
- Paper 1 details
- Paper 2 details

### Contact Information (Optional)
- Email: name@example.com
- Office: Building A, Room XXX (optional)
- Office Hours: Monday and Wednesday, 14:00-16:00 (optional)
```

### 3. Add Member Photo

Place member photos in the `assets/img/people/` directory:
- Filename: `NAME.jpg` or `NAME.png`
- Recommended size: 400x400 pixels (square) or 400x500 pixels (portrait)
- File size: Recommended less than 500KB

## Supported Social Media Links

The following links can be added in the `social` section:

- **email**: Email address
- **website**: Personal homepage URL
- **scholar_userid**: Google Scholar user ID
- **github_username**: GitHub username
- **linkedin_username**: LinkedIn username (part after /in/ in the URL)
- **twitter_username**: Twitter username (without @)
- **orcid_id**: ORCID ID (format: 0000-0000-0000-0000)
- **research_gate_profile**: ResearchGate profile name

## How to Get IDs from Different Platforms

### Google Scholar ID
1. Visit your Google Scholar profile page
2. URL format: `https://scholar.google.com/citations?user=YOUR_ID`
3. Copy the ID after `user=`

### LinkedIn Username
1. Visit your LinkedIn profile page
2. URL format: `https://www.linkedin.com/in/YOUR_USERNAME`
3. Copy the username after `/in/`

### ORCID ID
1. Visit your ORCID profile page
2. URL format: `https://orcid.org/0000-0000-0000-0000`
3. Copy the complete ID (including hyphens)

### ResearchGate Profile
1. Visit your ResearchGate profile page
2. URL format: `https://www.researchgate.net/profile/YOUR_NAME`
3. Copy the name after `/profile/`

## Page Ordering

The display order of members on the page is determined by their order in the `people.md` file. It's generally recommended to arrange them in the following order:
1. Principal Investigator (PI)
2. Postdoctoral Researchers
3. PhD Students
4. Master Students
5. Undergraduate Students
6. Alumni (optional)

## Style Customization

To modify the people page styles, you can edit the `.profile` related styles in the `_sass/_layout.scss` file.