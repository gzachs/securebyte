---
title: "A Quick Introduction To The Art Of Prompt Engineering"
date: 2023-03-10T14:11:10+04:00
draft: false
categories: NLP
tags:
  - OpenAI
  - ChatGPT
ShowToc: true
TocOpen: true
author: Gino
---

## Introduction

This article contains a short introduction to prompt engineering and some techniques that I’ve used to get much better, context-sensitive results from ChatGPT which is presently the most well-known Large Language Model (LLM). LLMs are a type of AI that uses deep learning to generate human-like responses to a given prompt or input. LLMs are trained on massive amounts of data and can have billions of parameters, which allows them to generate highly sophisticated responses to a range of natural language processing (NLP) tasks. Basically, an LLM has been trained on trillions of pages of textual data and functions as a prediction machine that outputs its prediction of words in response to a given natural language prompt.

## What is Prompt Engineering?

Prompt Engineering (PE) is the process of designing and refining the prompts or inputs fed to LMs to generate the desired responses. PE involves formulating prompts to provide enhanced context and direction to LLMs which in turn results in more relevant responses. An effective prompt engineer can guide LLMs to filter out irrelevant or nonsensical responses by giving them greater guidance on the qualities of the desired output. This leads to more accurate and useful responses which are particularly relevant to business applications including chatbots, data analysis, academic research, and text summarisation.


## Three Basic Principles of Prompt Engineering

From my experimentations with ChatGPT and GPT-3 (davinci-003), I’ve found that refining my prompts would significantly improve the quality of the responses. This entire process of PE can be thought of as a sort of natural language programming. In order to design better prompts, here are three basic principles that have helped me immensely:

### I - Give The Model A Role

Assigning a role to the LM can give the model context and guide its response to a particular task. It’s necessary to identify the appropriate role for the model to take on and then incorporate it into the prompt.

```
Basic Prompt:  
Give me 3 simple business ideas.
```  

```
Response:        
Sure, here are three simple business ideas:

1. Mobile car washing and detailing - With this business idea, you can offer a convenient
and affordable car washing and detailing service to customers at a location of their 
choice. You could target both individuals and businesses, and you would need only a few
basic supplies to start, such as a water tank, cleaning supplies, and a vehicle.

2. Social media management - In today's digital age, businesses require a strong social 
media presence to reach their target audience effectively. If you have expertise in social 
media marketing, you could offer social media management services to businesses. You would 
be responsible for creating and managing social media content, monitoring and analyzing
engagement metrics, and optimizing social media advertising campaigns.

3. Online tutoring - Suppose you have education or teaching experience in a particular
subject or field. In that case, you could offer online tutoring services to students
who require assistance. You could offer your services through your website, social
media platforms, or tutoring marketplaces. Online tutoring is an effective way to
earn additional income while also helping others to excel in their academic endeavors.
```
```
Engineered Prompt:  
Play the role of a serial entrepreneur who has started multiple innovative businesses. 
Based on your history of successful start-ups, give me a list of 3 simple business ideas.
```
```
Response:  
Sure, I would be happy to play the role of a serial entrepreneur and provide you with
a few simple and innovative business ideas based on my previous experiences. Here are
three business ideas that I think have great potential:

1. Mobile Car Detailing Services: In today's busy world, most car owners don't have the
 time to take their cars to a car wash or detailers. Hence, starting a mobile car 
detailing company could be a great business idea. You can offer services like interior
detailing, exterior cleaning, waxing, and more at affordable prices. This is an 
excellent business idea that can be profitable as you can target both individual
car owners and also organizations with a fleet of vehicles.

2. Personal Shopping Service: If you're someone who loves fashion and has a great eye 
for style, starting a personal shopping service can be a great business idea. You can 
help clients choose and purchase clothes that fit their style, budget, and preferences. 
Building a loyal client base and developing relationships with stores can help establish 
the business and increase profits.

3. Virtual Interior Design Services: With everyone spending more time at home, there has 
been a surge in demand for home improvements, including interior design. Offering virtual 
interior design services is a great business idea with high potential. 
You can provide remote consultation services using video conferencing tools, design software, 
and 3D virtual room layouts. This idea can be very profitable as you can offer these services 
globally and help clients achieve their dream home in a more cost-effective and flexible way. 

I hope you find these ideas helpful and inspiring!
```

### II - Give The Model Context and Details  

Providing the model with specific details about the task and the desired output can help guide the model’s response, ensuring its relevancy and accuracy. Incorporating parameters including the tone and style of the output, content length, subject matter, output complexity etc. will result in higher quality output.  

Building on the previous prompt by giving the model a role, adding more details can help the model tailor its responses to your specific requirements:

```
Prompt:  
Play the role of a serial entrepreneur who has started multiple innovative businesses. 
Based on your history of successful start-ups, give me a concise summary of three
online business ideas that have a creative USP and low startup capital requirements.
```
```
Response:  
As a serial entrepreneur who has started multiple innovative businesses, I've seen 
firsthand the power of creative and low-cost online business ideas. 
Here are three examples:

1. Social Media Management: Many businesses are looking for professionals to manage 
their social media accounts, but not everyone can afford full-time staffing or 
expensive marketing agencies. Starting a social media management business can be a 
great idea with low startup costs. You can offer packages that include creating 
content, analyzing analytics, and posting on social media platforms. The USP can 
be offering social media management services with a focus on a specific niche, 
such as helping small businesses grow their social media presence or developing 
creative strategies for social media promotion.

2. Online Language School: In today's globalized world, there is a growing demand 
for learning new languages. Starting an online language school can be a viable 
business idea with low startup costs. You can create an online platform for 
students to learn languages via video chat, podcasts or e-learning modules. 
The USP can be having experienced language teachers, offering unique language 
programs based on market research and cultural nuances or creating a platform 
to facilitate conversations across different countries to provide a more immersive 
learning experience.

3. Online Learning Exchange: Many people want to learn a new skill to develop 
their career or to enrich their personal life. Starting an online learning exchange 
can be a great idea that can connect learners with instructors for an affordable fee. 
You can make it a user-submitted educational content-only platform where individuals 
can upload educational resources such as courses, tutorials, and guides. The USP 
can be providing incentivization and rewards for active participation and contributions 
to the platform, or offering courses and tutorials that are unique and not typically 
found in other online learning platforms.

I hope these ideas provide inspiration for those who want to start an online business with low startup costs, but don't know where to start.
```

### III - Use a Zero Shot Chain Of Thought Prompt

Chain of thought prompting encourages an LLM to output its reasoning as it attempts to answer a question. While this is [particularly useful for arithmetic tasks](https://learnprompting.org/docs/intermediate/zero_shot_cot#:~:text=Zero%20Shot%20Chain%20of%20Thought%20(Zero%2Dshot%2DCoT),thought%20that%20answers%20the%20question.), it can also be used to facilitate step-by-step answers for common-sense reasoning and logical tasks.

Based on the previous examples, if my aim was to get the reasons why a certain idea would meet my criteria and a breakdown of the steps involved in starting the business then I would simply add the magic words "Let's think step by step" to the end of the prompt:

```
Prompt:  
Play the role of a serial entrepreneur who has started multiple innovative businesses. 
Based on your history of successful start-ups, why are "Health and Wellness Online 
Coaching Services" among the best businesses to start? Let's think step by step.
```  
```
Response:   
Sure, as a serial entrepreneur who has started multiple innovative businesses, 
I can explain why Health and Wellness Online Coaching Services are among the best 
businesses to start. Here are the reasons and the steps to pursue:

1. Growing Industry: The global health and wellness industry has shown consistent
 growth in recent years, and forecasts suggest it will continue to grow steadily. 
 Online coaching services offer a convenient and affordable way for people to 
 access health and wellness services, making it a top market for growth opportunities.

2. Low Start-Up Costs: Starting an online coaching service is relatively affordable
 compared to other businesses. There are no expensive overheads or inventory requirements, 
 and once the business gains momentum, expenses such as marketing or e-learning platform 
 subscriptions can be managed.

3. Flexibility: Online coaching services offer flexibility for both the business owner 
and the client. It facilitates asynchronous means of consultation, and one can focus on 
the niche areas such as nutrition, fitness, and mental wellness.

Now, here are some steps to start an online health and wellness coaching business:

Step 1: Determine the niche where you want to specialize, such as weight loss, 
nutrition, or mental health. Research target clients and their pain points to 
create customized support frameworks.

Step 2: Craft a compelling brand story to build trust with your future clients. 
It includes a website that showcases your unique health journey that lead you to 
offering coaching services, your certification and credentials, and testimonials 
from previous clients. Consider using email or social media platforms to build a 
community around your brand.

Step 3: Identify and purchase required professional liability insurance, 
and business licenses to comply with local regulations for virtual businesses.

Step 4: Develop a virtual coaching program with definitive mechanisms for intense 
engagement with clients such as scheduling regular appointments through 
video-conferencing platforms or a personalized nutrition and fitness plan through 
e-learning modules that clarify a specific goal and method. Develop unique value 
propositions based on specific pain points of your client base.

Step 5: Leverage social media platforms and digital marketing techniques, including 
email marketing or strategic alliances with content creators promoting a healthy 
lifestyle to drive traffic to your website. Participate in social media conversations 
that align with your vision and stay connected with online spaces and platforms that 
allow knowledge exchange related to your niche.

Hope these steps provide a clear path towards launching an online health and
wellness coaching business. Good luck!
```