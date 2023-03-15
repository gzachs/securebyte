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

From my experimentations with ChatGPT, I’ve found that refining my prompts would significantly improve the quality of the responses. This entire process of PE can be thought of as a sort of natural language programming. In order to design better prompts, here are three basic principles that have helped me immensely:

### I - Give The Model A Role

Assigning a role to the LM can give the model context and guide its response to a particular task. It’s necessary to identify the appropriate role for the model to take on and then incorporate it into the prompt.

```
Basic Prompt:  
Give me a list of three titles for a LinkedIn post.
```  

```
Response:        
1. "5 Strategies to Boost Your Productivity and Achieve Your Goals"
2. "Networking Tips for Introverts: How to Make Meaningful Connections"
3. "The Importance of Emotional Intelligence in the Workplace: How to Develop Yours"
```
```
Engineered Prompt:  
Pretend that you are a social media expert with extensive experience in crafting viral, creative titles for LinkedIn posts. Based on your expertise, give me a list of three titles for a LinkedIn post.
```
```
Response:  
Sure, here are three title suggestions based on my experience:

1. "The Surprising Benefits of Unplugging: Why Taking a Digital Detox Can Boost Your Productivity"
2. "The Power of Storytelling: How to Use Narrative to Connect with Customers and Build Your Brand"
3. "Mastering the Art of Work-Life Balance: Tips from Successful Entrepreneurs and CEOs"
```

While the second prompt is still quite vague, it nontheless draws out more specifics that can be areas of interest to focus on later.

### II - Give The Model Context and Details  

Providing the model with specific details about the task and the desired output can help guide the model’s response, ensuring its relevancy and accuracy. Incorporating parameters including the tone and style of the output, content length, subject matter, output complexity etc. will result in higher quality output.  

```
Basic Prompt:  
Come up with three ideas for a LinkedIn post. 
``` 
```
Response:      
Sure, here are three ideas for a LinkedIn post:

1. Share a personal success story: Write about a recent achievement you are proud of and how you overcame challenges to reach that goal. Be sure to mention any skills or strategies that helped you along the way, and how they could be applied to other situations. This type of post can inspire and motivate others in your network to pursue their own goals.

2. Highlight an industry trend: Share your thoughts on a current trend or issue in your industry. Discuss the potential implications of this trend and what it means for businesses and professionals in the field. By sharing your expertise, you can position yourself as a thought leader in your industry.

3. Offer career advice: Share tips and strategies for advancing in a particular field or industry. This could include advice on networking, building skills, or finding mentorship opportunities. By offering value to your connections, you can establish yourself as a helpful and knowledgeable member of your network.
```

Building on the previous prompt by giving the model a role, adding more details can help the model tailor its responses to your specific requirements:

```
Engineered Prompt:  
Pretend that you are a social media expert with extensive experience in crafting viral, creative LinkedIn posts. Based on your expertise, give me a concise summary of three ideas that are persuasive, compelling, and inspirational to the audience and will help me grow my network.
```
```
Response:  
As a social media expert with experience in crafting viral and creative LinkedIn posts, I would recommend the following three ideas that are persuasive, compelling, and inspirational to your audience, helping you grow your network:

1. Share a personal story of triumph: Everyone loves a good story, and sharing a personal story of triumph can be both inspiring and relatable to your audience. Talk about a time when you overcame a challenge in your career or personal life, and how that experience shaped you into the person you are today. By sharing your story, you'll create a human connection with your audience and establish yourself as someone who is relatable and trustworthy.

2. Offer valuable insights or tips: People use LinkedIn to learn and grow, so offering valuable insights or tips in your area of expertise is a great way to establish yourself as a thought leader and attract new followers. Share practical advice on how to overcome common challenges in your industry or tips for success in a particular role. This type of content not only helps your audience, but also positions you as someone who is knowledgeable and helpful.

3. Create a list of top industry influencers or resources: People love lists, and creating a list of top industry influencers or resources can be a great way to attract new followers and grow your network. Research and compile a list of the most influential people or resources in your industry, and share why you find them valuable. By creating this type of content, you'll establish yourself as someone who is well-connected and knowledgeable in your field.
```

### III - Use a Multi-Step Prompt

A multi-step prompt breaks down a complex task into multiple subtasks. Instead of asking the model to process the entire task in a single prompt, you can guide the model through a series of prompts where each prompt is designed to elicit information on the different subtasks. Then, you can ask the model to incorporate the information from the previous responses in the final prompt to produce more targeted content. Multi-step prompts are clearly useful for complex tasks where the model may have trouble understanding the desired output.

Based on the previous examples, if my aim was to get the best LinkedIn post ideas that had the chance to go viral AND the ability to attract recruiters, the following would be a suitable multi-step prompt:

```
Prompt:  
Play the role of a social media expert with extensive experience in crafting viral, creative LinkedIn posts. Based on your expertise, provide concise background information on the three most popular topics for LinkedIn posts.
```  

```
Response:      
As a social media expert with extensive experience in crafting viral, creative LinkedIn posts, I can tell you that there are three main topics that tend to perform exceptionally well on this platform:

Professional development: LinkedIn is the go-to social network for professionals looking to advance their careers, so it's no surprise that posts about professional development tend to perform well. This could include articles, videos, or other content related to industry trends, leadership, skill-building, or career advice. The key is to make the content actionable and valuable to your audience.

Company culture: People want to work for companies that share their values and culture. Sharing content that showcases your company's culture, such as team outings, company events, and employee spotlights, can be a great way to build your employer brand and attract top talent.

Thought leadership: LinkedIn is a platform where people come to learn and engage with thought leaders in their industry. Posts that showcase your expertise and unique perspective on industry trends, challenges, or opportunities can be a powerful way to build your personal brand and establish yourself as a go-to resource in your field.

Overall, the key to creating viral, creative LinkedIn posts is to focus on providing value to your audience. Whether it's professional development tips, company culture insights, or thought leadership on industry topics, your content should be educational, engaging, and relevant to your audience's interests and needs.
```
```
Prompt:  
Which three major particular aspects or sub-topics of these topics should I focus on to go viral?  
```

```
Response: 
Here are three specific sub-topics within each of the three main topics that could help your posts go viral on LinkedIn:

Professional development:  
Career advice: Share your own experiences and insights on how to advance your career or navigate challenges in the workplace.    
Skill-building: Offer tips and resources on how to improve skills that are in high demand within your industry.    
Industry trends: Discuss emerging trends or changes within your industry and provide your perspective on what they mean for professionals in your field.   

Company culture:  
Employee spotlights: Highlight individual employees or teams who are making a positive impact within the company.  
Corporate social responsibility: Share how your company is giving back to the community or contributing to social or environmental causes.  
Behind-the-scenes glimpses: Offer a peek into what makes your company unique, such as office decor, team-building activities, or office traditions. 
 
Thought leadership:  
Opinions on industry news: Share your perspective on the latest news within your industry and offer insights on what it means for the future.  
Data-driven insights: Use data or research to support your arguments or provide unique insights into your field.  
Future predictions: Offer your thoughts on where your industry is headed and provide ideas on how professionals can prepare for what's to come. 
   
Remember, no matter what sub-topics you choose to focus on, it's important to create content that is valuable, engaging, and relevant to your audience. By offering unique insights, sharing your expertise, and providing actionable tips or advice, you can increase the likelihood that your posts will go viral on LinkedIn.
```

```
Prompt:  
Based on the information you've provided so far, if I wanted to create a post which had the greatest potential to go viral and had the ability to attract the attention of recruiters, which three topics should I focus on?
```  
```
Response:   
If you want to create a post with the greatest potential to go viral and attract the attention of recruiters, I would recommend focusing on the following three topics:

Professional development: Posts related to professional development tend to perform well on LinkedIn and can showcase your knowledge and expertise to recruiters.
Consider sharing tips on how to advance your career, how to build skills that are in demand, or how to navigate challenges in the workplace.

Thought leadership: LinkedIn is a platform where people come to learn and engage with thought leaders in their industry. 
Sharing your unique perspective on industry trends, challenges, or opportunities can be a powerful way to establish yourself as a go-to resource in your field and attract the attention of recruiters who are looking for top talent.

Company culture: Recruiters want to work with candidates who not only have the right skills and experience but also share their company's values and culture. 
Posts that showcase your company culture, such as team outings, company events, or employee spotlights, can be a great way to build your employer brand and attract the attention of recruiters who are looking for candidates that align with their company culture.

Remember, to create a viral post that attracts the attention of recruiters, it's important to provide value to your audience and offer unique insights or perspectives. 
By sharing your expertise and showcasing your personality, you can increase the likelihood that your post will go viral and catch the attention of recruiters who are looking for top talent.
```


