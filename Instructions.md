# ⚠️🛑 IMPORTANT! IF YOU ARE UNSURE, MAKE A NEW BRANCH AND ONLY COMMIT TO THAT AND THEN PUH REQUEST INTO MAIN! OR ASK FOR HELP! 🛑⚠️

- [Template Documentation](https://greene-lab.gitbook.io/lab-website-template-docs)
- [Template GitHub](https://github.com/greenelab/lab-website-template)


<details>

<summary><B>📝 Guide: How to Add Your Profile to the DNS Lab Website</B></summary>

# 📝 Guide: How to Add Your Profile to the DNS Lab Website
Follow this step-by-step guide to add your profile page to our website repository on GitHub. No prior experience with Markdown or Jekyll is required—just follow the instructions below!

---

## 📌 Step 1: Create Your Markdown File

1. Navigate to the `/_members/` directory in this GitHub repository.
2. Click on the **Add file** button in the top-right corner and select **Create new file**.
3. Name your file using the format: `first-last.md` (lowercase, separated by hyphens).
   * *Example:* `shivani-kolekar.md`

---

## 📌 Step 2: Upload Your Profile Picture

1. Navigate to the `images/` (or `images/team/`) folder in the repository.
2. Click **Add file** -> **Upload files**.
3. Upload a square profile photo named after yourself (e.g., `shivani.png` or `shivani-kolekar.jpg`).
4. Note down the path to your image (e.g., `images/shivani.png`).

---

## 📌 Step 3: Fill Out Your File Information

Copy and paste the template below into your newly created `.md` file in `/_members/`, then edit the fields with your personal information.

### 📄 Copy-Paste Template

```yaml
---
name: Your Full Name
image: images/your-photo.png
role: phd
affiliation: Chonnam National University
links:
  email: your.email@example.com
  google-scholar: https://scholar.google.com/citations?user=YOUR_SCHOLAR_ID
  github: your-github-username
  linkedin: your-linkedin-profile
  home-page: https://your-personal-website.com
  cv: https://link-to-your-cv-or-resume-website.com
  thesis: https://link-to-your-thesis.com
---

Write a short bio about yourself here in Markdown syntax. 

Mention your degree program, research interests, past education, notable accomplishments, and current projects at DNS Lab. One to two paragraphs works best!
```

---

## 🛠️ Configuration Details & Options

### 1. `role` Field (Controls Page Category)
Set the `role` tag according to your current position so you appear in the correct section on the **Team** page:

| Value | Category |
| :--- | :--- |
| `professor` | Professor |
| `phd` | PhD Students |
| `master` | Master Students |
| `undergrad` | Undergraduate Students |

> **Note for Alumni:** If you have graduated and left the lab, add `group: alum` to your front matter metadata block.

### 2. Supported Links (`links:`)
You can include any of the following social/academic links under `links:`. *Make sure to indent them with two spaces!*

* `email`: `your-email@domain.com`
* `google-scholar`: ID of your Google Scholar profile
* `github`: Your GitHub username or full profile URL
* `linkedin`: Full URL to your LinkedIn profile
* `twitter`: Your Twitter handle (without `@`)
* `home-page`: URL to your personal website

---

## 💡 Example Profile

Here is a full example of what a completed member file looks like:

```yaml
---
name: Shivani Sanjay Kolekar
image: images/shivani.png
role: phd
affiliation: Chonnam National University
links:
  email: shivanikolekar@gmail.com
  google-scholar: _E95NsMAAAAJ
---

SHIVANI SANJAY KOLEKAR received the bachelor’s degree in computer science and engineering from Shivaji University, India, in 2020. She is currently pursuing the integrated M.S. and Ph.D. degree with the Department of Artificial Intelligence Convergence, Chonnam National University, Gwangju, South Korea. 

During her studies with Chonnam National University, she was a Teaching Assistant and a Research Assistant and also an Instructor through an international educational program. She has also been involved in interdisciplinary research on distributed systems for medical digital twins and AI models. Her research focuses on efficient artificial intelligence for networked and distributed systems, with particular interests in federated learning, communication-efficient learning, and fine-tuning large language models.
```

---

## 📌 Step 4: Save & Submit Changes

1. Scroll down to the **Commit changes...** section at the bottom of the page.
2. Add a commit message like: `Add Shivani Kolekar profile`.
3. Select **Commit directly to the `main` branch** (or open a Pull Request if required by repository settings).
4. Click **Commit changes**.

🎉 **Done!** The site will automatically build and update with your new profile page.
</details>

<details>

<summary><B>📚 Guide: How to Add Your Publications & Citations to the DNS Lab Website</B></summary>
  
# 📚 Guide: How to Add Your Publications & Citations to the DNS Lab Website

## NOTICE: We currently only list papers that have a DOI, via that DOI, and only papers in English!

This guide will show lab members step-by-step how to add, edit, or remove publications on the DNS Lab website. 

Our website uses **Manubot**, an automated citation generator. You only need to provide standard paper identifiers (like DOIs, arXiv IDs, or PubMed IDs), and the system will automatically fetch full titles, authors, journals, and publication dates for you!

---

## 📌 Method 1: Adding Publications by ID (Recommended)

Follow these steps to create or update your personal publications file.

### Step 1: Navigate to the Data Directory
1. Go to the `/_data/` folder in the repository on GitHub.
2. Check if a sources file already exists for you (e.g., `sources-shivani.yaml`). 
   * If it exists, click on it and click the **pencil icon (Edit this file)**.
   * If not, click **Add file** ➔ **Create new file** and name it using the format: `sources-yourname.yaml` (e.g., `sources-john.yaml`).

> ⚠️ **Important:** The filename MUST start with `sources-` and end with `.yaml`.

---

### Step 2: Add Your Citations

Paste your paper identifiers in YAML list format using `id: <identifier>`. 

#### 📄 Standard Template (Basic Identifiers)
```yaml
- id: doi:10.1109/ICAIIC60209.2024.10463204
- id: doi:10.1109/ICUFN57995.2023.10199942
- id: arxiv:1806.05726
- id: pubmed:29424689
```

Supported ID prefixes include:
* `doi:` (Digital Object Identifier)
* `arxiv:` (arXiv preprint ID)
* `pubmed:` (PubMed ID)
* `pmc:` or `pmcid:` (PubMed Central ID)
* `url:` or `isbn:`

---

<!--

### Step 3: Add Rich Details (Optional)

You can enhance how your paper appears on the site by adding extra fields such as project repo links, tags, descriptions, or custom thumbnail images:

```yaml
- id: doi:10.1109/ICAIIC60209.2024.10463204
  type: paper
  description: A novel framework for communication-efficient federated learning.
  image: images/publications/icaiic2024-thumb.png
  tags:
    - Federated Learning
    - Edge AI
  buttons:
    - type: source
      text: Code Repository
      link: https://github.com/CNU-DNS-Lab/your-repo
```

| Parameter | Description |
| :--- | :--- |
| `type` | Type of source (e.g., `paper`, `journal`, `conference`). Sets the icon shown. |
| `description` | Brief description or highlight of the work (supports Markdown). |
| `image` | Path or URL to a thumbnail image (figure, issue cover, or lab diagram). |
| `buttons` | Custom buttons to show underneath (e.g., link to code, dataset, or project website). |
| `tags` | List of topic tags to display underneath the paper details. |

---

## 📌 Method 2: Adding Your Entire ORCID Profile

If you keep your ORCID profile up to date, you can automatically import **all** of your publications at once.

1. Go to `/_data/` and open or create `orcid.yaml` (or `orcid-members.yaml`).
2. Add your ORCID ID and a unique identifier tag for filtering:

```yaml
- orcid: 0000-0002-4655-3773
  shivani-kolekar: true
```

---

## 📌 How to Correct or Remove an Automatically Imported Citation

If Manubot fetches inaccurate citation data or includes a paper you don't want displayed:

### To Override Incorrect Data:
In your `sources-yourname.yaml` file, manually specify the correct field:
```yaml
- id: doi:10.1109/ICAIIC60209.2024.10463204
  title: "Corrected Title of the Paper Here"
```

### To Remove an Unwanted Paper:
In your `sources-yourname.yaml` file, add `remove: true`:
```yaml
- id: doi:10.1109/ICAIIC60209.2024.10463204
  remove: true
```

---

## 📌 Method 3: Manual Entry (No DOI/ID Available)

If your paper or report does not have a DOI or online ID yet, you can enter all the details manually:

```yaml
- title: "An Overview of Medical Digital Twins in Distributed Systems"
  authors:
    - "**Shivani Sanjay Kolekar**"
    - "Co-Author Name"
  publisher: "Chonnam National University Technical Report"
  date: 2024-05-15
  link: https://example.com/paper.pdf
```

-->

---

## 📌 Step 4: Save & Build

1. Scroll down to the **Commit changes...** section at the bottom of GitHub.
2. Write a short commit message (e.g., `Add new ICAIIC 2024 paper for Shivani`).
3. Click **Commit changes**.

> ⏱️ **Note:** Do NOT edit `/_data/citations.yaml` directly! GitHub Actions will automatically run the build process in the background, run Manubot to collect metadata for all IDs, and overwrite `citations.yaml` automatically.

</details>


<details>

<summary><B>🛠️ Guide: How to Add Projects & Datasets to the DNS Lab Website</B></summary>

# 🛠️ Guide: How to Add Projects & Datasets to the DNS Lab Website
This guide provides step-by-step instructions for members of **DNS Lab** to add open-source projects, datasets, software tools, and repositories to the lab website.

---

## 📌 Step 1: Open the Projects Data File

Projects on the website are managed through a single YAML file located at:

```text
/_data/projects.yaml
```

1. Navigate to the `/_data/` directory in the repository on GitHub.
2. Click on `projects.yaml`.
3. Click the **Pencil Icon** (✏️ *Edit this file*) in the top-right corner.

---

## 📌 Step 2: Add Your Project Entry

Scroll to the bottom of `projects.yaml` and add a new entry following the template below:

### 📄 Copy-Paste Template

```yaml
- title: Your Project Name
  subtitle: A short one-line summary or tag-line
  group: featured
  image: images/your-project-thumbnail.png
  link: https://github.com/CNU-DNS-Lab/your-repo-name
  description: A detailed description of what the software, dataset, or tool does, how to use it, or what findings it supports.
  repo: CNU-DNS-Lab/your-repo-name
  tags:
    - software
```

---

## 🛠️ Field Reference & Customization

| Field | Required? | Description | Example |
| :--- | :--- | :--- | :--- |
| **`title`** | **Yes** | Name of the project, tool, or dataset. | `PLDC-80 Dataset` |
| **`subtitle`** | Optional | Brief tagline shown below the title. | `Benchmarking Dataset for Plant Leaf Disease Classification` |
| **`group`** | Optional | Set to `featured` to highlight prominent projects on the home page or top section. | `featured` |
| **`image`** | Optional | Path to a preview thumbnail image (square aspect ratio recommended). | `images/pldc80.png` |
| **`link`** | **Yes** | Primary URL where users can access the code, paper, or dataset. | `https://github.com/CNU-DNS-Lab/PLDC-Net` |
| **`description`** | **Yes** | 1–3 sentence summary explaining the project. Supports Markdown formatting. | `This repository includes code for the PLDC-Net architecture...` |
| **`repo`** | Optional | GitHub repository path (`organization/repo-name`). Displays live repo stats (e.g. stars/forks) if enabled. | `CNU-DNS-Lab/PLDC-Net` |
| **`tags`** | Optional | Tag list for site filtering (`software`, `dataset`, `publication`, `resource`). | `- dataset` |

---

## 💡 Real Example Entries

Here are two example entries as structured in `/_data/projects.yaml`:

```yaml
- title: PLDC-80 Dataset
  subtitle: Benchmarking Dataset for Plant Leaf Disease Classification
  group: featured
  image: images/pldc80.png
  link: https://github.com/CNU-DNS-Lab/PLDC-Net
  description: Instructions for building PLDC-80, a Benchmarking Dataset for Plant Leaf Disease Classification, from public sources.
  repo: CNU-DNS-Lab/PLDC-Net
  tags:
    - dataset

- title: PLDC-Net
  subtitle: PLDC-Net implemented using TensorFlow and Keras
  group: featured
  image: images/pldcnet.png
  link: https://github.com/CNU-DNS-Lab/PLDC-Net
  description: This repository includes the code for the architecture of PLDC-Net as well as a script with the setup to train it. The default parameters are set to be the same as they were in the paper when the model was trained on PLDC-80.
  repo: CNU-DNS-Lab/PLDC-Net
  tags:
    - software
```

---

## 🖼️ Uploading a Project Image (Optional)

If your project includes a thumbnail (`image: images/your-project.png`):

1. Go to the `images/` directory in the repo.
2. Click **Add file** ➔ **Upload files**.
3. Upload your image (PNG or JPG).
4. Commit the image file directly to the `main` branch.

---

## 📌 Step 3: Save & Commit Changes

1. Scroll to the **Commit changes...** box at the bottom of GitHub.
2. Add a clear commit message, e.g.:
   ```text
   Add new PLDC-Net project to projects.yaml
   ```
3. Select **Commit directly to the `main` branch** (or open a pull request).
4. Click **Commit changes**.

🎉 **Done!** GitHub Pages will build your changes and display the new project on the site automatically.

</details>


<details>

<summary><B>📝 Guide: How to Add a Blog Post to the Lab Website</B></summary>

# 📝 Guide: How to Add a Blog Post to the Lab Website

Follow this step-by-step, foolproof guide to write and publish a new blog post on our lab website. 

---

## Step 1: Navigate to the Posts Folder
1. Go to our repository on GitHub.
2. Open the **`_posts`** directory. (This is where all blog posts live).

---

## Step 2: Create a New File
1. Click the **"Add file"** button near the top right of the file list and select **"Create new file"**.
2. Name your file using the mandatory Jekyll naming convention:
   
   `YYYY-MM-DD-your-post-title.md`
   
   * **Example:** `2026-10-02-new-research-breakthrough.md`
   * **🚨 CRITICAL:** The date format (`YYYY-MM-DD`) at the beginning of the filename is required. The website template uses this to automatically set the post's URL and publication date!

---

## Step 3: Copy and Fill Out the Template
Paste the following template directly into your new empty file and fill in your specific details:

```markdown
---
title: "Your Awesome Post Title Here"
image: images/your-thumbnail-filename.png
author: your-username
tags: tag1, tag2, tag3
---

<!-- excerpt start -->
This is the short summary paragraph that shows up on the main Blog page preview card. Make it catchy!
<!-- excerpt end -->

Write the rest of your full blog post content down here using standard Markdown. 

You can add standard paragraphs, add links like [this one to Google](https://google.com), and embed images:

![Description of image for screen readers](images/your-image.png)
```

---

## Step 4: Understand the Configuration (Front Matter)

At the very top of your file, between the `---` dashes, are your settings. Here is what they mean:

| Parameter | Description | Example |
| :--- | :--- | :--- |
| `title` | **Required.** The main headline of your post. | `title: New Dataset Released` |
| `image` | **Optional.** Path to your thumbnail/header image. Store your images in the repo's `images/` folder. | `image: images/pldc80.png` |
| `author` | **Optional.** Your team member ID (the exact filename of your profile page **without** the `.md` extension). This automatically links your photo and name. | `author: david` |
| `tags` | **Optional.** Comma-separated list of topics for filtering. | `tags: agriculture, computer-vision` |

---

## Step 5: Setting the Preview Excerpt
When people visit the main Blog page, they see a preview card for your post. You have two ways to define what text shows up there:

1. **The recommended way:** Wrap your summary text in `<!-- excerpt start -->` and `<!-- excerpt end -->` right inside the body of your post (as shown in the template above).
2. **The lazy way:** If you don't add those tags, the website will automatically grab the very first paragraph of your post and use that as the preview.

---

## Step 6: Save and Publish
1. Scroll down to the **"Commit changes..."** button at the top or bottom of the page.
2. Write a short, descriptive commit message (e.g., `Add blog post about PLDC-80 dataset`).
3. Select **Commit directly to the `main` branch** (unless you are using pull requests).
4. Click the green **Commit changes** button.

🎉 **That's it!** Once committed, GitHub Pages will automatically build the site, and your new post will be live on the website within a minute or two.

</details>
