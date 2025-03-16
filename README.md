# Social-Media-Complaint-Analysis-using-R
Analyzed the impact of social media content types and self-featured posts on engagement using linear regression and instrumental variables to address endogeneity.

![image](https://github.com/user-attachments/assets/6df18642-fe3d-46ac-880c-2fb01cf49259)


## Project Background

This project investigates how social media content characteristics impact customer engagement when posting complaints. Inspired by the viral "United Breaks Guitars" case, the analysis explores whether content type (video vs. image) and featuring oneself influence engagement levels. The project leverages both linear regression and instrumental variables (IV) regression for more accurate results.

## Problem Statement

Social media has become a key platform for customer complaints. This project addresses:

Whether video content leads to more engagement than static images.

Whether featuring oneself in a complaint post influences engagement.

How unobserved factors may introduce endogeneity, affecting conclusions.

## Key Questions

Does posting a video vs. image impact likes and comments?

Does featuring oneself vs. the offender influence engagement levels?

Are these relationships confounded by unobserved factors, requiring an instrumental variables approach?

## Data Overview

The dataset includes:

IGLikes: Number of likes received per post

IGComments: Number of comments received per post

Video: Binary indicator for video content

FeatureSelf: Binary indicator for featuring oneself in the post

Followers: Number of followers the poster has

LengthChar: Length of the text in characters

Photography: Proportion of prior posts with camera emoji/photography hashtag (instrument for video)

SelfPct: Proportion of prior posts featuring oneself (instrument for featuring oneself)

## Methodology

Data Cleaning & Preparation: Prepared key variables, ensuring consistency across observations.

Descriptive Analysis: Examined the distribution of key variables for insights.

Correlation Analysis: Evaluated relationships between engagement metrics and predictors.

Linear Regression Analysis: Measured direct relationships.

Instrumental Variables (IV) Regression: Addressed endogeneity concerns to improve causal inference.

Model Comparison: Compared OLS and IV estimates to highlight the value of proper instrumentation.

## Key Findings & Insights

### 1. Impact of Videos on Engagement

Videos were associated with higher engagement, but OLS results were biased due to endogeneity.

IV regression showed a negative effect for videos once unobserved confounders were controlled.

![image](https://github.com/user-attachments/assets/d54943ec-a9cc-4a59-9909-62c3d43cb237)


### 2. Impact of Featuring Oneself on Engagement

Featuring oneself significantly increased likes and comments.

IV regression confirmed this finding with improved reliability.

![image](https://github.com/user-attachments/assets/0d81ba09-af42-463c-b422-91a740e59e2f)


### 3. Correlation Analysis

Positive correlations were observed between photography habits and video posting, confirming its validity as an instrument.

A strong relationship between self-featured content and engagement reinforced the relevance of using SelfPct as an instrument.

![image](https://github.com/user-attachments/assets/7fa0c376-a823-4f9c-8862-a57aa859f2bf)


### 4. Model Comparison

IV regression improved estimates by correcting for endogeneity, highlighting the need for appropriate instruments in causal inference.

![image](https://github.com/user-attachments/assets/8b995201-957a-46d3-829d-0375224db08e)


## Conclusion

The analysis found that videos were less effective for engagement than initially believed when accounting for endogeneity. Featuring oneself consistently led to higher engagement. Proper instrumentation proved critical in drawing accurate conclusions.

## Recommendations

Companies should consider promoting content that features individuals for improved engagement.

Relying solely on video content may not guarantee better performance; marketers should diversify their strategies.

Future research should explore content tone, emotion, and brand perception as additional influencers on engagement.

