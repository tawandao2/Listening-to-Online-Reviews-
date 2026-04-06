# Listening-to-Online-Reviews-
Data analysis project, listening to online reviews for Saphora 
# Project Summary 
This project provides a strategic analysis of over 1,500 consumer reviews for L’Occitane and La Mer to decode the drivers of brand equity and customer loyalty in the prestige skincare market. By applying VADER Sentiment Analysis and Natural Language Processing (NLP) in R, I identified that while La Mer maintains a slightly higher average rating of 4.06, L’Occitane excels in "sensory storytelling," with customers frequently detailing the ritualistic experience of the products. A key finding revealed that 1-star reviews are significantly longer than 5-star reviews, acting as a diagnostic blueprint for product improvement, while dry skin emerged as the primary demographic for high satisfaction across both brands. These data-driven insights culminate in a proposed Starbucks x L’Occitane "Fast Beauty" subscription box, which leverages the STEPPS framework to transform daily coffee rituals into high-engagement skincare moments. 

# Data Description & Star Distributions 
The dataset consists of over 1,500 customer reviews for luxury skincare brands (L'Occitane and La Mer). The Mean Star Rating is 4.04, indicating a generally positive customer sentiment.

# Data Description & Star Distributions 
The dataset consists of over 1,500 customer reviews for luxury skincare brands (L'Occitane and La Mer). The Mean Star Rating is 4.04, indicating a generally positive customer sentiment.

<img width="1009" height="667" alt="image" src="https://github.com/user-attachments/assets/12745e2a-8d0f-484e-97dc-8c416ffd4955" />
The distribution of review lengths shows that most reviews are relatively short, with a long tail of very lengthy entries. The average review length is about 404 characters, which means anything above this value can reasonably be considered a “long” review, while anything below it is a “short” review. This distinction helps us compare how sentiment differs between brief comments and more detailed, expressive reviews.

## Analysis of 1-Star Reviews
<img width="489" height="145" alt="image" src="https://github.com/user-attachments/assets/32ae5c50-352c-4c39-b65e-a5dcafe7d75f" />
For one‑star reviews, longer reviews show noticeably less negative sentiment than shorter ones. The average compound VADER score for long 1‑star reviews is about 0.302, compared to only 0.098 for short reviews. Long reviews also contain slightly more positive language and slightly less negative language. This suggests that even when customers give the lowest rating, those who write longer reviews tend to express their dissatisfaction in a more balanced or nuanced way, while short 1‑star reviews are more sharply negative.

## Statistical significance test (1‑star long vs short)
<img width="481" height="210" alt="image" src="https://github.com/user-attachments/assets/a92b02a7-94ba-4380-aac2-c67579305128" />
A statistical comparison between long and short one‑star reviews shows that the difference in sentiment is meaningful. The Welch t‑test returns a p‑value of 0.029, indicating that long and short reviews differ significantly in their average compound VADER sentiment. Long one‑star reviews are noticeably less negative (mean compound ≈ 0.302) than short one‑star reviews (mean compound ≈ 0.098). This supports the idea that even unhappy customers tend to express themselves in a more balanced, less emotionally extreme way when they write longer reviews.

## 5‑star reviews
<img width="514" height="295" alt="image" src="https://github.com/user-attachments/assets/5a839da2-58ac-46d2-bada-85c74f2f583a" />
For five‑star reviews, longer reviews express significantly stronger positive sentiment than shorter ones. Long reviews have a much higher average compound VADER score (≈0.832) compared to short reviews (≈0.688), indicating that customers who write more tend to use richer, more enthusiastic language. The Welch t‑test confirms that this difference is highly statistically significant (p ≈ 3.1e‑11). In other words, satisfied customers become even more positive when they take the time to write longer, more detailed reviews.

# Brand Insights & Social Media Strategy
## Average Sentiment by Rating (Bar Chart)
Sentiment increases steadily with rating level. Five‑star reviews show strongly positive compound sentiment, while one‑star reviews are sharply negative. This confirms that customers’ emotional tone aligns closely with their rating behavior.
Because sentiment tracks cleanly with ratings, the brand can confidently use sentiment monitoring as an early warning system. Sudden drops in sentiment even before ratings fall may signal emerging product issues or shifts in customer expectations.
<img width="493" height="183" alt="image" src="https://github.com/user-attachments/assets/2c46f073-c323-4b13-ae62-ff4d71ae9192" />

## Average Sentiment by Rating
Most reviews are relatively short, with a long tail of very lengthy reviews. The average review length is about 404 characters, meaning most customers leave brief comments while a smaller group writes detailed, thoughtful feedback.
Short reviews tend to be emotionally extreme (very positive or very negative), while long reviews contain richer insights. The brand should monitor long reviews for deep product feedback and treat short reviews as emotional signals that may require quick customer support responses.
<img width="719" height="273" alt="image" src="https://github.com/user-attachments/assets/35b22d8c-378d-46e4-8a98-5e092c527b2c" />

## Review Length Distribution
<img width="444" height="364" alt="image" src="https://github.com/user-attachments/assets/202d72b6-829c-4a3b-97ba-0676f0946086" />
This chart compares the average compound sentiment of long versus short reviews. Long reviews show noticeably higher sentiment scores, meaning customers who write more tend to express more positive or balanced emotions. Short reviews, on the other hand, are more emotionally intense and skew more negative. This pattern suggests that longer reviews provide richer, more thoughtful feedback, while short reviews often reflect quick, emotional reactions.

## Sentiment Comparison: L’Occitane vs La Mer
L’Occitane and La Mer both earn strong praise from customers, but their reviews reveal different strengths. La Mer’s feedback skews slightly more positive overall, with reviewers highlighting luxurious textures, rich hydration, and a noticeable glow. L’Occitane’s high‑rating reviews focus on gentle formulas, pleasant scents, and reliable everyday performance. When customers are dissatisfied, L’Occitane tends to receive comments about dryness or lack of results, while La Mer’s complaints center on heaviness, greasiness, or price. Together, these insights show that L’Occitane wins on approachability and comfort, while La Mer leads on indulgence and perceived effectiveness giving each brand a distinct emotional space in the skincare market.
<img width="510" height="132" alt="image" src="https://github.com/user-attachments/assets/34eab4d7-3039-4fc7-97ed-7e31877ac77c" />

## Rating‑ratio comparison (4–5 vs 1–2 stars)
La Mer consistently shows stronger reviewer sentiment than L’Occitane across both text‑based and rating‑based metrics. VADER analysis reveals that La Mer’s reviews carry a slightly more positive emotional tone on average, and the rating ratio confirms this advantage: La Mer receives over four times as many 4–5‑star reviews as 1–2‑star reviews, compared with a three‑to‑one ratio for L’Occitane. Together, these results suggest that while both brands are well‑liked, La Mer inspires more enthusiastic satisfaction overall, whereas L’Occitane’s feedback is positive but more mixed.
<img width="498" height="148" alt="image" src="https://github.com/user-attachments/assets/81d95a10-a283-4a6f-9ed5-7b3d77e55c00" />

## Word clouds: high vs low ratings, by brand

<img width="779" height="656" alt="image" src="https://github.com/user-attachments/assets/6dece4f2-9ea4-4f38-9c56-829c10d38508" />
Across both brands, the word‑cloud patterns reveal clear differences in what drives satisfaction and frustration for customers. L’Occitane’s high‑rating reviews highlight soft textures, pleasant scents, and gentle moisturizers, while its low‑rating reviews focus on issues like smell, oiliness, and irritation. La Mer’s positive reviews emphasize rich creams, hydration, and overall product quality, whereas its negative reviews frequently mention price, dryness, and disappointment with results. Together, these patterns show that L’Occitane wins praise for comfort and sensory appeal, while La Mer earns enthusiasm for performance—yet also faces sharper criticism when expectations aren’t met

## Parts of speech: adjectives in satisfied vs dissatisfied review
<img width="804" height="511" alt="image" src="https://github.com/user-attachments/assets/4868e666-d95f-4245-8a97-ebf1ee586c10" />
In L’Occitane’s low‑rating reviews, customers frequently use adjectives like oily, thick, dry, strong, and sensitive, revealing a pattern of texture and skin‑reaction concerns. Even positive‑leaning words such as great, nice, and good appear in this group, suggesting that some reviewers appreciate certain aspects of the products but still experience issues that lead to lower ratings. Overall, the language indicates that dissatisfied customers tend to struggle with heaviness, oiliness, or irritation, pointing to opportunities for L’Occitane to refine formulations for sensitive or combination skin types.

## Top Adjectives Used in High‑Rating L’Occitane Reviews
<img width="823" height="455" alt="image" src="https://github.com/user-attachments/assets/77ac49c7-9dc8-4914-b9b1-ceb6ccd1537e" />
 L’Occitane’s high‑rating reviews, customers consistently use adjectives like amazing, soft, great, smooth, and worth, highlighting a strong appreciation for texture, comfort, and overall product experience. Even words like oily and dry appear in this group, suggesting that while some users note specific skin‑type interactions, they still view the products positively overall. The frequent appearance of terms such as expensive and worth also shows that satisfied customers often feel the quality justifies the price. Altogether, the language paints a picture of products that deliver a pleasant sensory feel and reliable performance for most user

 # Starbucks x Fast Beauty Seasonal Subscription Box
## AI‑Generated Customer‑Centric Concept Report
To design a seasonal beauty subscription box that feels authentic to Starbucks customers, we apply the Customer‑Centric Framework: understand customer emotions, seasonal needs, and the rituals Starbucks already owns. Seasonal drinks already symbolize emotional states—renewal in Spring, brightness in Summer, comfort in Fall, and indulgence in Winter. Translating these cues into beauty themes creates a subscription box that feels intuitive, fun, and aligned with customer behavior.


## Spring — Matcha Renewal
Inspired by: Iced Matcha Latte
Theme: Fresh start, gentle detox, soft glow
Recommended products: green tea sheet masks, hydrating gel creams, dewy facial mists
Why: Customers seek calming, lightweight hydration after winter dryness.


## Summer — Pink Drink Radiance
Inspired by: The Pink Drink
Theme: Bright, fruity, energetic
Recommended products: vitamin C serums, SPF sticks, shimmer body mists
Why: Summer shoppers prioritize radiance, sun protection, and travel‑friendly essentials.


## Fall — Pumpkin Spice Comfort
Inspired by: Pumpkin Spice Latte
Theme: Cozy, warm, barrier‑repair
Recommended products: oat masks, rich creams, vanilla‑spice lip oils
Why: Fall customers want nourishment, comfort textures, and seasonal scents.


## Winter — Peppermint Mocha Glow
Inspired by: Peppermint Mocha
Theme: Indulgence, hydration, holiday sparkle
Recommended products: deep moisturizers, peppermint lip treatments, festive highlighters
Why: Winter skin needs moisture, and holiday shoppers love sensory experiences.


 # Additional Data & Analytics to Strengthen the Strategy
To refine product selection and ensure each box resonates, additional analytics would deepen customer understanding:

## Customer Behavior
1. Seasonal purchase patterns

2. Product affinity (items frequently bought together)

3. Repeat‑purchase likelihood by category

## Customer Segmentation
1. Skin type, tone, age, lifestyle clusters

2. Starbucks Rewards behavioral segments

3. Social persona mapping (glow‑seekers, minimalists, ingredient‑focused shoppers)

## Value & Pricing Analytics
1. Willingness‑to‑pay modeling

2. Sentiment‑weighted product scoring

3. Perceived value vs. cost optimization

## Seasonal Skin Needs
1. Dryness, oiliness, sensitivity patterns by season

2. Ingredient sentiment (e.g., caffeine, green tea, niacinamide)


# Additional Data to Collect
1. Starbucks Rewards surveys on scent, texture, and skin concerns

2. In‑app click behavior on beauty content

3. Social listening around seasonal drinks + beauty trends

4. Regional climate data (humidity, UV index, temperature)


# Final Product Recommendations
Based on customer sentiment, seasonal emotions, and Starbucks’ brand identity, the recommended product strategy includes:

1. Hydration‑first skincare across all seasons

2. Seasonal scent and texture variants tied to Starbucks drinks

3. Travel‑friendly minis for convenience and perceived value

4. Ingredient‑forward products (green tea, caffeine, oat, vitamin C)

5. One “fun” seasonal item per box (lip oil, shimmer stick, limited scent)


























