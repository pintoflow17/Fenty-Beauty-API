# Fenty Beauty API Documentation

The Fenty Beauty API provides access to product information, collections, and search functionality for Fenty Beauty's catalog. This API allows you to retrieve detailed product information, search products, and browse collections.

## Authentication

To use this API, you'll need:
1. A RapidAPI account
2. Subscribe to the [Fenty Beauty API on RapidAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/fenty-beauty-api)
3. Your RapidAPI key (add in the headers as `X-RapidAPI-Key`)

## Base URL
```
https://fenty-beauty-api.p.rapidapi.com
```

## Endpoints

### 1. List Products
Get a paginated list of all products.

```
GET /products
```

**Parameters:**
- `page` (optional): Page number (default: 1)
- `perPage` (optional): Items per page (default: 250, max: 250)
- `country` (optional): Country code (default: 'us')

**Example Response:**
```json
{
    "products": [
        {
            "title": "Product Name",
            "price": "35.00",
            "description": "Product description",
            // ... additional product details
        }
    ],
    "pagination": {
        "currentPage": 1,
        "totalPages": 10
    }
}
```

### 2. Get Product Details
Retrieve detailed information about a specific product.

```
GET /products/details
```

**Parameters:**
- `productUrl` (required): Full URL of the product

**Example Response:**
```json
{
    "title": "Product Name",
    "description": "Detailed product description",
    "price": "35.00",
    "images": [],
    "variants": [],
    // ... additional product details
}
```

### 3. Get Product URLs
Retrieve a list of product URLs for further processing.

```
GET /products/urls
```

**Parameters:**
- `page` (optional): Page number (default: 1)
- `perPage` (optional): Items per page (default: 35)
- `country` (optional): Country code (default: 'us')

### 4. Search Products
Search for products in the catalog.

```
GET /search
```

**Parameters:**
- `query` (required): Search term
- `page` (optional): Page number (default: 1)
- `perPage` (optional): Items per page (default: 35)
- `country` (optional): Country code (default: 'us')

### 5. List Collections
Get all available product collections.

```
GET /collection
```

**Parameters:**
- `page` (optional): Page number (default: 1)
- `country` (optional): Country code (default: 'us')

### 6. Get Collection Products
Retrieve products from a specific collection.

```
GET /collection/products
```

**Parameters:**
- `collectionsHandle` (optional): Collection identifier (default: 'new-arrivals')
- `page` (optional): Page number (default: 1)
- `country` (optional): Country code (default: 'us')

## Error Handling

The API returns standard HTTP status codes:
- 200: Success
- 400: Bad Request (missing or invalid parameters)
- 401: Unauthorized (invalid API key)
- 404: Not Found
- 500: Internal Server Error

Error Response Format:
```json
{
    "error": {
        "message": "Error message",
        "code": "400"
    }
}
```

## Rate Limiting

Please refer to your RapidAPI subscription tier for specific rate limiting details.

## Code Examples

### JavaScript/Node.js
```javascript
const axios = require('axios');

const options = {
  method: 'GET',
  url: 'https://fenty-beauty-api.p.rapidapi.com/products',
  params: {
    page: '1',
    perPage: '35',
    country: 'us'
  },
  headers: {
    'X-RapidAPI-Key': 'YOUR_RAPIDAPI_KEY',
    'X-RapidAPI-Host': 'fenty-beauty-api.p.rapidapi.com'
  }
};

try {
    const response = await axios.request(options);
    console.log(response.data);
} catch (error) {
    console.error(error);
}
```
---
## Support
- pintoflowpt@gmail.com
---
**All About Fenty Beauty: Revolutionizing the Beauty Industry**

Founded in 2017 by music and fashion icon Rihanna, Fenty Beauty was created with a groundbreaking mission: to provide high-quality, inclusive beauty products that cater to all skin types and tones. Since its inception, Fenty Beauty has reshaped the beauty landscape, prioritizing diversity and self-expression. From its award-winning foundations to its innovative lipsticks and highlighters, Fenty Beauty continues to set new standards for excellence and inclusivity in the beauty industry.

### **The Vision Behind Fenty Beauty**

Rihanna’s inspiration for creating Fenty Beauty stemmed from her personal experience. As someone who struggled to find products that worked for her skin tone, she wanted to ensure that everyone, regardless of their complexion, could find makeup that made them feel confident and beautiful.

Fenty Beauty’s tagline, "Beauty for All," reflects this commitment. The brand’s debut product, the Pro Filt’r Soft Matte Longwear Foundation, launched with 40 shades, a revolutionary move at the time. Today, Fenty Beauty’s foundation range has expanded to over 50 shades, making it one of the most inclusive beauty brands globally.

---

### **Fenty Beauty’s Iconic Products**

**1. Pro Filt'r Soft Matte Longwear Foundation**
- Known for its buildable coverage, matte finish, and extensive shade range, this foundation is a staple in many makeup kits.

**2. Gloss Bomb Universal Lip Luminizer**
- This lip gloss delivers a non-sticky, high-shine finish. Available in a variety of shades, it suits all skin tones, making it a cult favorite.

**3. Killawatt Freestyle Highlighter**
- With shades ranging from subtle champagne to bold golds, the Killawatt Highlighter is perfect for adding a radiant glow.

**4. Match Stix Matte and Shimmer Skinsticks**
- These versatile sticks can be used for contouring, concealing, or adding a pop of shimmer to the skin.

**5. Fenty Skin Hydra Vizor Invisible Moisturizer SPF 30**
- Part of the Fenty Skin line, this moisturizer combines hydration and sun protection, leaving a dewy finish without a white cast.

---

### **Fenty Beauty’s Commitment to Inclusivity**

Inclusivity is at the core of Fenty Beauty. Beyond offering a wide range of shades, the brand also prioritizes accessibility in marketing and representation. Campaigns feature models of different ethnicities, ages, and body types, showcasing the versatility of Fenty Beauty’s products. This approach has resonated deeply with consumers, fostering a sense of belonging and authenticity.

---

### **Fenty Skin: Expanding Into Skincare**

In 2020, Rihanna introduced Fenty Skin, a skincare line designed to complement the Fenty Beauty collection. The products are vegan, cruelty-free, and formulated with globally sourced ingredients. Some standout products include:

- **Total Cleans'r Remove-It-All Cleanser**: A gentle yet effective cleanser suitable for all skin types.
- **Fat Water Pore-Refining Toner Serum**: A multitasking product that brightens, refines pores, and hydrates the skin.
- **Instant Reset Overnight Recovery Gel-Cream**: A rich, non-greasy moisturizer that revitalizes the skin overnight.

---

### **Frequently Asked Questions About Fenty Beauty**

#### **1. Where can I buy Fenty Beauty products?**
Fenty Beauty products are available at Sephora, Harvey Nichols, and the brand’s official website, fentybeauty.com. They are also sold at select retailers globally.

#### **2. Are Fenty Beauty products cruelty-free?**
Yes, Fenty Beauty is a cruelty-free brand. None of its products are tested on animals.

#### **3. Are Fenty Beauty products vegan?**
While many Fenty Beauty products are vegan, not all are. The brand provides clear labeling for vegan products on its website.

#### **4. How do I find my shade in Fenty Beauty foundations?**
Fenty Beauty offers an online shade finder tool and encourages customers to visit stores for in-person shade matching. The brand also provides comprehensive guides to help users select the right undertone.

#### **5. What makes Fenty Beauty’s foundation unique?**
The Pro Filt’r Foundation is known for its lightweight, long-lasting formula and extensive shade range, catering to various undertones and skin types.

#### **6. Does Fenty Beauty offer sustainable packaging?**
Yes, Fenty Beauty and Fenty Skin are committed to sustainability. Many products come in refillable packaging, and the brand uses recyclable materials wherever possible.

#### **7. Can I use Fenty Beauty if I have sensitive skin?**
Fenty Beauty products are formulated to be suitable for various skin types, including sensitive skin. However, it’s always recommended to check ingredient lists and perform patch tests.

#### **8. Are there any tips for applying Fenty Beauty products?**
- Use a damp sponge or Fenty’s Precision Makeup Sponge for a flawless foundation application.
- Pair the Pro Filt’r Foundation with the Pro Filt’r Primer for a smooth base.
- Layer the Killawatt Highlighter for an intense glow or use a light hand for a subtle shimmer.

---

### **Awards and Recognition**

Fenty Beauty has received numerous accolades, including:

- **Time Magazine’s Best Inventions of 2017**: Recognized for its innovation and inclusivity.
- **Allure Best of Beauty Awards**: Multiple products, including the foundation and highlighters, have been honored.
- **CFDA Fashion Icon Award**: Although primarily a fashion accolade, Rihanna’s work with Fenty Beauty has solidified her influence in the beauty industry.

---

### **How Fenty Beauty Is Changing the Beauty Industry**

**1. Setting a Standard for Inclusivity:**
Fenty Beauty’s expansive shade range has inspired other brands to follow suit, leading to a more inclusive industry overall.

**2. Combining Beauty and Skincare:**
Products like the Eaze Drop Blurring Skin Tint blur the line between makeup and skincare, offering a hybrid solution for modern consumers.

**3. Emphasizing Sustainability:**
By introducing refillable packaging and environmentally conscious practices, Fenty Beauty is paving the way for a more sustainable beauty industry.

**4. Championing Diversity in Marketing:**
Fenty Beauty’s campaigns celebrate diversity, featuring individuals from all walks of life, reinforcing the brand’s core values.

---

### **Customer Testimonials**

- **Emily T.**: “I’ve always struggled to find a foundation that matches my skin tone perfectly. Fenty Beauty’s Pro Filt’r changed the game for me. It’s lightweight, buildable, and lasts all day!”

- **Jordan M.**: “The Gloss Bomb is my holy grail. It’s hydrating, non-sticky, and makes my lips look amazing. Plus, the shades are universally flattering.”

- **Sofia L.**: “As someone with sensitive skin, I was skeptical at first. But Fenty Skin’s Hydra Vizor is a lifesaver. It’s moisturizing without feeling greasy, and the SPF is a bonus!”

---

### **Conclusion**

Fenty Beauty is more than just a makeup brand; it’s a movement that celebrates individuality, diversity, and innovation. With a growing range of products and a steadfast commitment to inclusivity, Fenty Beauty has set a new benchmark in the beauty industry. Whether you’re a makeup enthusiast or someone just starting their beauty journey, Fenty Beauty offers something for everyone.

Explore the world of Fenty Beauty today and discover why it’s loved by millions worldwide!

