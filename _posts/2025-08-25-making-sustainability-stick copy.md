---
layout: post
title:  "Making sustainability stick"
date:   2025-08-25 12:00:00 +0200
categories: green
description: Using the Web Sustainability Guidelines to have constructive discussions
---

As an expert (in accessibility, sustainability, etc.), it is often tempting to answer “no” to some ideas and proposals. This is not necessarily the best approach, as this article suggests: [Making accessibility stick](https://buttondown.com/access-ability/archive/how-to-make-accessibility-stick/).  

# Learning to stop saying “no”
The article in question focuses on accessibility and draws on the [WCAG (Web Content Accessibility Guidelines) from the W3C (World Wide Web Consortium)](https://www.w3.org/WAI/standards-guidelines/wcag/) to suggest more constructive alternatives through specific examples. In short, as an accessibility expert, it can be tempting to say “no,” especially to certain design proposals (carousels, infinite scrolling, etc.). I'll let you read the article in detail. Here, we will focus on how these considerations apply to sustainability. To do this, we will use the [WSG (Web Sustainability Guidelines) from the W3C](https://w3c.github.io/sustainableweb-wsg/).  

**A quick note on the WSG** : this repository of sustainability best practices is being elaborated by web sustainability experts through an [Interest Group](https://www.w3.org/groups/ig/sustainableweb/), with the purpose of producing web sustainability standards in the near future. Everyone there is awesome and nice so feel free to contribute!   
Now, back to our topic.  
 
First of all, it is important to emphasize that saying “no” often short-circuits discussions and can lead to deadlock or even animosity. When the expert is called in too late (on a digital service that has already been deployed or on finalized mock-ups), changes may appear too costly. Perhaps the proposed element is non-negotiable for certain stakeholders (business, communication, etc.). In such cases, “no” is not always acceptable.  
 
The idea is not to let anything go, but to suggest ways to make the proposal more straightforward and/or efficient, or even to define the framework for arriving at an acceptable solution (changing the Definition of Done or acceptance tests, for instance). And to offer help in achieving this.  
 
## Common examples
### The carousel
**What they asked:** what could be better than images automatically scrolling horizontally to catch the eye of the user?  
**My response:** [https://shouldiuseacarousel.com/](https://shouldiuseacarousel.com/) (and I suggested adding a mosaic of images instead, with an example here: [https://www.musba-bordeaux.fr/](https://www.musba-bordeaux.fr/))   
We know that this type of component is often bad for eco-design (and for accessibility and even more generally for the user experience). Rather than simply rejecting it outright, it is better to define a few best practices to follow:  
* Avoid adding unnecessary complexity: **[2.6 Minimize non-essential content, interactivity, or journeys](https://w3c.github.io/sustainableweb-wsg/#minimize-non-essential-content-interactivity-or-journeys)**  
* Decorative design should be beneficial to the user (and avoid being detrimental to sustainability): **[2.7 Use decorative design with care](https://w3c.github.io/sustainableweb-wsg/#use-decorative-design-with-care)**
* Attention is better than distraction: **[2.9 Be attentive rather than distracting](https://w3c.github.io/sustainableweb-wsg/#be-attentive-rather-than-distracting)**  
* Optimize displayed content: **[2.15 All images must be optimized for sustainability](https://w3c.github.io/sustainableweb-wsg/#all-images-must-be-optimized-for-sustainability)**
* Use animation with care (and avoid it if possible): **[2.17 Animation must be proportionate and easy to control](https://w3c.github.io/sustainableweb-wsg/#animation-must-be-proportionate-and-easy-to-control)**
  
In addition, here are some tips for improving the user experience: [https://www.smashingmagazine.com/2022/04/designing-better-carousel-ux](https://www.smashingmagazine.com/2022/04/designing-better-carousel-ux) 
 
In the case of a simple animation, this criterion is also essential to take into account. In addition to the absence of automatic triggering, the duration of the animation will be important. Beyond 4 seconds, control mechanisms must be put in place. For more information on this subject:
 
* [https://greenspector.com/en/analysis-of-overconsumptions-on-a-light-website-2/](https://greenspector.com/en/analysis-of-overconsumptions-on-a-light-website-2/)
* [https://greenspector.com/en/reduce-the-weight-of-a-web-page-which-elements-have-the-greatest-impact/](https://greenspector.com/en/reduce-the-weight-of-a-web-page-which-elements-have-the-greatest-impact/)  
  

### Infinite scrolling  
**What they asked:** we have a lot of elements to highlight, especially since we create new ones very often. An infinite list will allow us to have everything in one place.  
**My response:** you're going to overwhelm the user with information and they won't go beyond the first few items.  
Infinite scrolling is everywhere on social media, but also often on news and e-commerce sites. Be sure to keep these criteria in mind:  
* Keep content easily findable: **[2.8 Ensure that navigation and way-finding are well-structured](https://w3c.github.io/sustainableweb-wsg/#ensure-that-navigation-and-way-finding-are-well-structured)**  
* Attention is better than distraction: **[2.9 Be attentive rather than distracting](https://w3c.github.io/sustainableweb-wsg/#be-attentive-rather-than-distracting)**. It even has its own Success Criterion : **Avoid attention-keeping**.
* Optimize displayed content: **[2.15 All images must be optimized for sustainability](https://w3c.github.io/sustainableweb-wsg/#all-images-must-be-optimized-for-sustainability)**   
  
In addition, it is important for the user to know how the displayed elements are selected, sorted, and filtered. And to be able to change this if necessary.
  
  
### The interactive map
**What they asked:** if we're going to show information about places, we might as well rely on a ready-to-use, interactive component.
**My response:** That's not a good idea. In fact, I'm usually already at the “yes, but” stage. I recommend avoiding Google Maps (very heavy in terms of environmental impact and risky in terms of GDPR and accessibility). If you have to choose, go for OpenStreetMap instead. In addition, I recommend using a facade (display a default image and only load the map when the user interacts with it). [https://developer.chrome.com/docs/lighthouse/performance/third-party-facades](https://developer.chrome.com/docs/lighthouse/performance/third-party-facades)  

In addition to these recommendations, you can refer to these recommentations:  
* Avoid adding unnecessary complexity: **[2.6 Minimize non-essential content, interactivity, or journeys](https://w3c.github.io/sustainableweb-wsg/#minimize-non-essential-content-interactivity-or-journeys)**  
* Accessibility first: **[2.21 Consider the impact of visitors using non-visual browsers](https://w3c.github.io/sustainableweb-wsg/#consider-the-impact-of-visitors-using-non-visual-browsers)**  
* Be aware of the real added value of components: **[2.27 Ensure features provide maximum value for their impact](https://w3c.github.io/sustainableweb-wsg/#ensure-features-provide-maximum-value-for-their-impact)**  
* Assess the impacts of third-party services: **[3.6 Third-party services should be assessed as first parties](https://w3c.github.io/sustainableweb-wsg/#third-party-services-should-be-assessed-as-first-parties)**  
  
In addition, provide an accessible version of the information on the map, for example in the form of a simple list (with the option to sort, filter, or search if necessary). If possible, the list can be offered as the default view. If there are only a few locations to display (as is sometimes the case on pages showing how to contact a company), it is best to opt for a simple postal address (or even an image showing the location).  

### Artificial intelligence and its derivatives  
**What they asked:** to make it easier for users to find information, we are going to set up a chat bot.  
**My response:** the environmental impact is likely to be considerable. And most of if will be hard to assess, especially on the server (and training) side.  
   
Twenty years ago, forums were everywhere. Social media feeds followed. Chatbots are now taking over and growing rapidly. If such a component needs to be implemented, the WSG is also a valuable source of information. As for previous items seen here, you can rely on recommendations **2.6, 2.21, 2.27 and 3.6**.  
  
## Some principles to fuel the discussion
* Show understanding: it is not necessarily about what you want or don't want as an expert. The priority is to support the client so that what they want meets the sustainability criteria   
* Point to specific WSG criteria and, if necessary, to other references, [GR491](https://gr491.isit-europe.org/en/) or [RWEB](https://rweb.greenit.fr/en)  
* Suggest proven alternatives, with examples  
* If possible, introduce sustainability criteria for component validation  
* Use these discussions to raise awareness on sustainability and help your contacts move forward on this topic  
  
## Conclusion
Rather than restricting, why not seize this opportunity to open up the discussion and help your contacts learn more about sustainability? Everyone will come out happier and having learned something new. As a bonus, as an expert, you will go from being the person who always complains and blocks progress to the person who helps everyone move in the right direction.