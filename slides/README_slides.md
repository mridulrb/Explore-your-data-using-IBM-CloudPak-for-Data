---
jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: myst
      format_version: '1.1'
      jupytext_version: 1.1.0
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---
<!-- 
+++ {"slideshow": {"slide_type": "slide"}} -->

<!-- # Tutorial slides

- Slides are optional (e.g., you may not use them if your presentation is via live coding).
- If the pre-recorded presentations will use slides, we request that you deposit the slides in this folder. 

<!-- 
## Use text-based source

- We ask that you use text-based formats for your slides, e.g., markdown 
- This markdown file is an example source for slides using `nbconvert` and Reveal. See the GitHub action '.github/workflows/slides.yml' in this repo so see how this markdown file is converted to a HTML slide show and published on GitHub Pages - https://fawazsiddiqi.github.io/slides_to_pages

+++ {"slideshow": {"slide_type": "subslide"}}

## An example sub-slide

- Another option: you can write your slide content using markdown and use an app for slide design, like [Deckset](https://www.deckset.com) or similar.

+++ {"slideshow": {"slide_type": "slide"}}

## Naming convention and file list

- Use a **naming convention** where each file name starts with a number, reflecting the order of use in the presentation of the tutorial.
- List your slide files in a markdown, with a brief description.


+++ {"slideshow": {"slide_type": "slide"}} 
-->

**Details** <br />
Using IBM Watson Studio and Watson Machine Learning, this code pattern provides an example of data science workflow which attempts to predict the end-of-day value of S&P 500 stocks based on historical data. This pattern includes the data mining process that uses the Quandl API – a marketplace for financial, economic, and alternative data delivered in modern formats for today’s analysts.

🎓 Learning outcomes
- Use Jupyter Notebooks in Watson Studio to mine financial data using public APIs.
- Use specialized Watson Studio tools like Data Refinery to prepare data for model training.
- Build, train, and save a time series model from extracted data, using open-source Python libraries or the built-in graphical -Modeler Flow in Watson Studio.
- Interact with IBM Cloud Object Storage to store and access mined and modeled data.
- Store a model created with Modeler Flow and interact with the Watson Machine Learning service using the Python API.
- Generate graphical visualizations of time series data using Pandas and Bokeh.

+++ {"slideshow": {"slide_type": "subslide"}}

🎙Speakers
- Mridul Bhandari, IBM Developer Advocate, https://developer.ibm.com/profiles/mridul.bhandari/
- Anchal Bhalla, Data and AI Technical Specialist, https://developer.ibm.com/profiles/anchal.bhalla/

🎈Prerequisites
- IBM Cloud Sign-up link - http://ibm.biz/StockMarketWatsonStudio
- Register for the live event or watch the recording: https://www.crowdcast.io/e/forecast-stock-market

👩‍💻Resources
- Hands-on - https://ibm.biz/StockMarketWatsonStudioLab
- GitHub Repository - https://github.com/IBM/watson-stock-market-predictor
- Survey - https://www.surveymonkey.com/r/JHT3L8Y
- Meetup page: https://www.meetup.com/IBM-Cloud-MEA/events/ 


+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide1.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide2.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide3.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide4.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide5.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide6.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide7.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide8.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide9.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide10.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide11.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide12.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide13.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide14.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide15.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide16.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide17.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide18.png?raw=true)

+++ {"slideshow": {"slide_type": "slide"}}

![center](https://github.com/mridulrb/watson-stock-market-predictor/blob/master/images/slide_images/Slide19.png?raw=true)


## License

**Recommend** that slides be shared under a [CC-BY](https://creativecommons.org/licenses/by/4.0/) license.
