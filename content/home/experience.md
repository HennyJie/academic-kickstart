+++
# Experience widget.
widget = "experience"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 45  # Order that this section will appear.

title = "Experience"
subtitle = ""

# Date format for experience
#   Refer to https://sourcethemes.com/academic/docs/customization/#date-format
date_format = "Jan 2006"

# Experiences.
#   Add/remove as many `[[experience]]` blocks below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin/end multi-line descriptions with 3 quotes `"""`.
[[experience]]
  title = "Research Intern"
  company = "Sensetime"
  company_url = "https://www.sensetime.com/en/"
  location = "Beijing, China"
  date_start = "2018-12-18"
  date_end = "2019-7-15"
  description = """
  Worked with [Chris Xiaoxuan Lu](http://www.cs.ox.ac.uk/people/xiaoxuan.lu/) to build a Face and Speech Recognition System with surveillance cameras and microphones:
  
  * Proposed a method using Wi-Fi appearance information to label images and audio automatically in the wild by Python programming.
  * Designed and implemented a pipeline framework to label capturing images and fine-tune the model.
  """

[[experience]]
  title = "Mitacs Global Research Intern"
  company = "Queens University"
  company_url = "http://perk.cs.queensu.ca/"
  location = "Kingston, Cananda"
  date_start = "2018-07-25"
  date_end = "2018-10-15"
  description = """Used machine learning algorithms(NLP, One-Class SVM) to detect malicious commands in Linux:

  * Loaded data in multiple threads from NFS among firm.
  * Got every available commands’ manual page to get the corpus and build LSI Model. Used NLP to remove stop words(some of the most common, short function words).
  * Used AdaBoost to detect outlier in One-Class SVM.
  """

+++
