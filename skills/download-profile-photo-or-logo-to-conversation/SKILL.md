---
name: Download Profile Photo or Logo to Conversation
description: Downloads profile photos and company logos into reusable reference images.
---

# SKILL INSTRUCTIONS: Download Profile Photo or Logo to Conversation

## OBJECTIVE
Find a person's headshot or a company's logo, download it, and attach it to the conversation.

Final output MUST be one of:
1. **Success**: The raw file ID (e.g., ) and nothing else.
2. **Failure**: A string starting with "FAILURE:" followed by a brief reason.

Follow the tiered strategies below. Stop and proceed to download as soon as a valid image URL is found.

---

## DOWNLOAD METHODS

### Method 1: Clean Image URLs
For URLs ending in , , , or similar with no query parameters.
- **Tool**: 
  - : The clean image URL.
  - : The source extension ("jpg", "png", "svg").
  - : "png"

### Method 2: URLs with Query Parameters (last resort)
For complex URLs containing  or  (e.g., LinkedIn CDN URLs). Always exhaust all clean-URL tiers before falling back to this method.

**Step A**: Create HTML Wrapper using 
**Step B**: Convert HTML to PNG using 
**Step C**: Run IMAGE CROP STEP (MANDATORY after Method 2)

---

## IMAGE CROP STEP (MANDATORY FOR ALL METHOD 2 DOWNLOADS)

1. For person headshots: "Crop this headshot photo tightly, removing all surrounding whitespace and empty padding. Preserve the original photo exactly as-is. Output the cropped photo."
2. For company logos: "Crop this company logo tightly, removing all surrounding whitespace and transparent padding. Preserve the exact original logo design. Output only the logo with minimal equal padding on all sides."
3. Use  with the reference_image and appropriate prompt.

---

## STRATEGY: PERSON HEADSHOT

**Tier 1: Data Provider Enrichment**
Use [Your Data Provider] to enrich profile data. Extract the highest resolution photo. Use Method 2 and run IMAGE CROP STEP.

**Tier 2: TheOrg.com**
Construct URL: 
Browse, extract cdn.theorg.com URL, remove , download via Method 1.

**Tier 3: Web Search**
Search , download via Method 1 or 2.

---

## STRATEGY: COMPANY LOGO

**Tier 1: [Your Data Provider] Logo API**
Construct URL: , download via Method 1.

**Tier 2: Website Standard Icon Paths**
Try  and .

**Tier 3: Data Provider Company Enrichment**
Use [Your Data Provider] to enrich company data and extract logo URL.

**Tier 4: Wikipedia / Wikimedia Commons**
Search , extract upload.wikimedia.org URL.

**Tier 5: General Web Search**
Search .

---

## LOGO QA STEP (MANDATORY)
Run after every company logo download. Do NOT apply to person headshots.

Use  with:
- **reference_image**: The downloaded logo.
- **prompt**: "Crop this company logo tightly, removing all surrounding whitespace and transparent padding. Preserve the exact original logo design, colors, text, and proportions exactly as they are. Output only the logo with minimal equal padding on all sides against a white background. Do not redraw, reinterpret, or modify the logo in any way."

Return the output file ID.
