+++

# Experience widget.

widget = "experience" # See https://sourcethemes.com/academic/docs/page-builder/
headless = true # This file represents a page section.
active = true # Activate this widget? true/false
weight = 40 # Order that this section will appear.

title = "Experience"
subtitle = ""

# Date format for experience

# Refer to https://sourcethemes.com/academic/docs/customization/#date-format

date_format = "Jan 2006"

# Experiences.

# Add/remove as many `[[experience]]` blocks below as you like.

# Required fields are `title`, `company`, and `date_start`.

# Leave `date_end` empty if it's your current employer.

# Begin/end multi-line descriptions with 3 quotes `"""`.

[[experience]] title = "Research Assistant" company = "University of Oxford" company_url = "https://www.cs.ox.ac.uk/" location = "Oxford, UK" date_start = "2018-09-08" date_end = "2019-09-30" description = """ Worked with Chris Xiaoxuan Lu to build a Face and Speech Recognition System with surveillance cameras and microphones:

Proposed a method using Wi-Fi appearance information to label images and audio automatically in the wild by Python programming.
Designed and implemented a pipeline framework to label capturing images and fine-tune the model. """

[[experience]] title = "Technology Summer Analyst" company = "Morgan Stanley" company_url = "https://www.morganstanley.com/" location = "Shanghai, China" date_start = "2018-07-09" date_end = "2018-09-07" description = """Used machine learning algorithms(NLP, One-Class SVM) to detect malicious commands in Linux:

Loaded data in multiple threads from NFS among firm.
Got every available commands’ manual page to get the corpus and build LSI Model. Used NLP to remove stop words(some of the most common, short function words).
Used AdaBoost to detect outlier in One-Class SVM. """




+++
