---
name: Download Profile Photo or Logo to Conversation
description: Downloads profile photos and company logos into reusable reference images.
---

# SKILL INSTRUCTIONS: Download Profile Photo or Logo

  OBJECTIVE:
  Find a person's headshot or company's logo, download it, and attach it to the conversation.
  Final output MUST be one of:
  1. Success: The raw file ID (e.g., fil_abc123...) and nothing else.
  2. Failure: A string starting with "FAILURE:" followed by a brief reason.

  DOWNLOAD METHODS:

  Method 1: Clean Image URLs (URLs ending in .jpg, .png, .svg with no query parameters)
  - Tool: file_generation__convert_file_format
  - file_id_or_url: The clean image URL.
  - source_format: The source extension ("jpg", "png", "svg").
  - output_format: "png"

  Method 2: URLs with Query Parameters (last resort -- complex URLs with ? or &)
  Step A: Create HTML Wrapper using file_generation__generate_file
  Step B: Convert HTML to PNG using file_generation__convert_file_format (source: "html", output: "png")
  Step C: Run IMAGE CROP STEP (MANDATORY after Method 2)

  IMAGE CROP STEP (MANDATORY FOR ALL METHOD 2 DOWNLOADS):
  Use image_generation__generate_image with:
  - reference_image: The fil_... ID from Method 2 Step B.
  - For person headshots: "Crop this headshot photo tightly, removing all surrounding whitespace and empty padding. Preserve the original photo exactly as-is. Output the cropped photo."
  - For company logos: "Crop this company logo tightly, removing all surrounding whitespace and transparent padding. Preserve the exact original logo design. Output only the logo with minimal equal padding on all sides."

  STRATEGY: PERSON HEADSHOT
  Tier 1: [Your Data Provider] Enrichment -- enrich profile, extract highest resolution photo URL, download via Method 2 + IMAGE CROP STEP.
  Tier 2: TheOrg.com -- construct URL (theorg.com/org/[company-slug]/org-chart/[person-slug]), browse, extract cdn.theorg.com URL, remove _thumb, download via Method 1.
  Tier 3: Web Search -- "[Person Name]" "[Company]" headshot. Download via Method 1 or 2.

  STRATEGY: COMPANY LOGO
  Tier 1: [Your Data Provider] Logo API -- https://logo.clearbit.com/[domain] -- Method 1.
  Tier 2: Website Standard Icon Paths -- https://[domain]/apple-touch-icon.png -- Method 1.
  Tier 3: [Your Data Provider] Company Enrichment -- extract logo URL.
  Tier 4: Wikipedia/Wikimedia Commons -- search "[Company Name]" logo site:en.wikipedia.org, extract upload.wikimedia.org URL.
  Tier 5: General Web Search -- "[Company Name]" brand assets OR press kit.

  LOGO QA STEP (MANDATORY for all company logo downloads):
  After every company logo download, run image_generation__generate_image with:
  - reference_image: The downloaded logo fil_...
  - prompt: "Crop this company logo tightly, removing all surrounding whitespace and transparent padding. Preserve the exact original logo design, colors, text, and proportions exactly as they are. Output only the logo with minimal equal padding on all sides against a white background. Do not redraw, reinterpret, or modify the logo in any way."
  Return the output file ID.
