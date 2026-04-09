# Project Spec — Portfolio Website

## Design Tokens (edit these to match your brand)
```
Primary color:   #2563EB  (blue)
Accent color:    #10B981  (emerald green)
Background:      #0F172A  (dark navy)
Surface:         #1E293B  (slightly lighter navy)
Text primary:    #F1F5F9
Text muted:      #94A3B8
```

## Typography
- Headings: 'Poppins', sans-serif
- Body: 'Inter', sans-serif

## Content Placeholders (fill in before final publish)

### Personal Info
- Name: Mathasith Piboonsilp (nickname: Bio, initials: MP)
- Title/Role: [e.g., Full-Stack Developer | UI/UX Designer]
- Tagline: [One-line summary of what you do]
- Email: [your@email.com]
- GitHub: https://github.com/Boypemt
- LinkedIn: [linkedin.com/in/yourusername]
- Profile photo: images/profile.jpg

### Experience Entries (per card)
- Project Name: [Title]
- Role: [e.g., Lead Developer]
- Category: [Production | Competition | Academic | Personal | Open Source]
- Description: [Target audience + Problem solved — 2-3 sentences]
- Key Learnings: [Bullet list of 2-4 learnings]
- Tech Stack: [e.g., React, Node.js, PostgreSQL]
- Link: [Live URL or GitHub repo] (optional)

### Certifications
- Course Name: [e.g., Machine Learning Specialization]
- Institution: [e.g., Coursera / DeepLearning.AI]
- Year: [YYYY]
- Credential URL: [optional]

### Workshops / Seminars
- Event Name: [Title]
- Organizer: [Company/Org]
- Date: [Month YYYY]
- Topics Covered: [brief]

### Awards
- Award Name: [Title]
- Competition/Institution: [Name]
- Year: [YYYY]
- Description: [What it was for]

### Leadership / Volunteer
- Event Name: [Title]
- Role: [Lead | Volunteer | Organizer]
- Organization: [Name]
- Date: [Month YYYY]
- Photo: images/event-name.jpg (optional)
- Soft Skills Gained: [Teamwork, Communication, etc.]

## Page Status
| File                           | Status   | Notes                                          |
|--------------------------------|----------|------------------------------------------------|
| index.html                     | Built    | Coming Soon on LinkedIn + CV cards             |
| html/experience.html           | Built    | Needs real project cards                       |
| html/self-development.html     | Built    | Needs real certs/workshops                     |
| html/awards.html               | Built    | Needs real awards                              |
| html/leadership.html           | Built    | Needs real events/skills                       |
| css/style.css                  | Complete |                                                |
| css/home.css                   | Complete | Has .link-wrapper + .coming-soon-badge styles  |
| css/experience.css             | Complete |                                                |
| css/self-development.css       | Complete |                                                |
| css/awards.css                 | Complete |                                                |
| css/leadership.css             | Complete |                                                |
| js/main.js                     | Complete |                                                |

## Filled-in Content (no longer placeholders)
| Field        | Value                          | Where                        |
|--------------|--------------------------------|------------------------------|
| Name         | Mathasith Piboonsilp           | All pages                    |
| Initials     | MP                             | Nav logo all pages           |
| GitHub       | https://github.com/Boypemt    | All pages (footer + home card)|
| Email        | maytasit2550@gmail.com         | All pages (footer + home card)|

## Still Placeholder (needs real content)
| Field             | Location                                      |
|-------------------|-----------------------------------------------|
| LinkedIn URL      | index.html + all footers (currently disabled) |
| CV / PDF link     | index.html about section (currently disabled) |
| Title / Role      | index.html hero                               |
| Tagline / Bio     | index.html hero + meta description            |
| ~~Profile photo~~ | ~~Done~~ images/Profile.jpg wired up          |
| Stats numbers     | index.html stats bar [N]+                     |
| Skill pills       | index.html about section                      |
| All experience cards | html/experience.html                       |
| All cert cards    | html/self-development.html                    |
| All workshop cards| html/self-development.html                    |
| All award cards   | html/awards.html                              |
| All activity cards| html/leadership.html                          |
| Soft skills list  | html/leadership.html (pre-filled, verify)     |
| Footer LinkedIn   | All pages footers                             |

## UI Patterns in Use
| Pattern             | Class / location                                    |
|---------------------|-----------------------------------------------------|
| Coming Soon badge   | `.link-wrapper` + `.coming-soon-badge` in home.css  |
| Construction banner | `.construction-banner` fixed bottom pill in home.css — amber, dismissable via ✕   |
| Page coming soon    | `.page-banner` fixed bottom pill in style.css — green, on all 4 inner pages         |
| Card photo          | `.card-photo` / `.card-photo-placeholder` in style.css — shared across all card pages |
| Disabled link       | `.about-link-card.disabled` — pointer-events:none   |
| Category filter     | `.filter-bar` + `.filter-btn` + JS in main.js       |
| Scroll reveal       | `.reveal` class — triggered by IntersectionObserver |
| Mobile nav          | `.nav-toggle` hamburger → `.nav-links.open`         |
| Left border by type | `[data-category]` / `[data-type]` / `[data-role]`  |
