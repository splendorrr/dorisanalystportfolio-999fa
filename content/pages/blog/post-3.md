---
'0':
  type: string
  name: layout
  label: Layout
  const: PostLayout
  hidden: true
'1':
  type: string
  name: metaTitle
  label: Title meta tag (overrides title)
  description: >-
    By default, the <title> tag for this page is determined by the title field
    (in the Content group). You can override the tag value here.
  default: null
  group: seo
'2':
  type: boolean
  name: addTitleSuffix
  label: Add title suffix
  description: >-
    If enabled, the title suffix defined in the site configuration is appended
    to the title tag of this page.
  default: true
  group: seo
'3':
  type: list
  name: metaTags
  label: Additional meta tags
  description: >-
    To add or override any meta tag for this page, add entries to this list.
    Entries defined here take precedence over any other defaults.
  group: seo
  items:
    type: model
    models:
      - MetaTag
'4':
  type: string
  name: title
  label: Title
  default: This is a blog post title
  required: true
'5':
  type: enum
  name: colors
  label: Colors
  group: styles
  controlType: palette
  options:
    - label: Colors A
      value: colors-a
      textColor: $onLight
      backgroundColor: $light
      borderColor: '#ececec'
    - label: Colors B
      value: colors-b
      textColor: $onDark
      backgroundColor: $dark
      borderColor: '#ececec'
    - label: Colors C
      value: colors-c
      textColor: $onSecondary
      backgroundColor: $secondary
      borderColor: '#ececec'
    - label: Colors D
      value: colors-d
      textColor: $onComplementary
      backgroundColor: $complementary
      borderColor: '#ececec'
    - label: Colors E
      value: colors-e
      textColor: $onComplementaryAlt
      backgroundColor: $complementaryAlt
      borderColor: '#ececec'
  default: colors-d
'6':
  type: date
  name: date
  label: Date
  required: true
'7':
  type: reference
  name: author
  label: Author
  models:
    - Person
'8':
  type: string
  name: excerpt
  label: Excerpt
  default: >-
    Nunc rutrum felis dui, ut consequat sapien scelerisque vel. Integer
    condimentum dignissim justo vel faucibus.
'9':
  type: model
  name: featuredImage
  label: Featured image
  models:
    - ImageBlock
  default:
    type: ImageBlock
    url: 'https://assets.stackbit.com/components/images/default/post-4.jpeg'
    altText: Post thumbnail image
    caption: ''
'10':
  type: model
  name: media
  label: Media
  models:
    - ImageBlock
    - VideoBlock
  default:
    type: ImageBlock
    url: 'https://assets.stackbit.com/components/images/default/post-4.jpeg'
    altText: Post image
'11':
  type: list
  name: bottomSections
  label: Sections
  items:
    type: model
    models:
      - ContactSection
      - CtaSection
      - DividerSection
      - FeatureHighlightSection
      - FeaturedItemsSection
      - FeaturedPeopleSection
      - FeaturedPostsSection
      - HeroSection
      - MediaGallerySection
      - QuoteSection
      - RecentPostsSection
      - TestimonialsSection
      - TextSection
'12':
  type: string
  name: metaDescription
  label: 'Description tag (default: excerpt)'
  description: >-
    By default, the description tag for this post is taken from the Excerpt
    field. You can override the tag value here.
  default: null
  group: seo
'13':
  type: image
  name: socialImage
  label: 'Image for social (default:  featured image)'
  description: >-
    By default, the "og:image" meta tag set for social sharing this post points
    to the Featured Image field (in the Content group). You can override that
    image here.
  default: null
  group: seo
'14':
  type: markdown
  name: markdown_content
  label: Content
  description: Page content
layout: PostLayout
metaTitle: null
addTitleSuffix: true
metaTags: []
title: 'STATA: The Effect of Region on Mental Health'
colors: colors-c
date: '2022-11-18'
excerpt: >-
  Econometrics Research Paper that shows the impact of where we live in the
  United States  on our mental health. I used 4 regions in the US: north,
  northeast, south and west. 
featuredImage:
  type: ImageBlock
  url: /images/bg.jpg
  altText: Post Thumbnail Image
media:
  type: ImageBlock
  url: /images/bg.webp
  altText: Post Image
bottomSections:
  - elementId: ''
    variant: variant-d
    colors: colors-d
    title: Read next
    showDate: true
    showAuthor: false
    showExcerpt: true
    recentCount: 3
    styles:
      self:
        height: auto
        width: wide
        margin:
          - mt-0
          - mb-0
          - ml-0
          - mr-0
        padding:
          - pt-12
          - pb-56
          - pr-4
          - pl-4
        justifyContent: center
      title:
        textAlign: center
      subtitle:
        textAlign: center
      actions:
        justifyContent: center
    type: RecentPostsSection
  - type: DividerSection
    colors: colors-d
    styles:
      self:
        width: wide
        padding:
          - pt-4
          - pb-4
          - pl-4
          - pr-4
        justifyContent: center
        borderWidth: 1
        borderStyle: solid
  - type: FeaturedPostsSection
    colors: colors-d
    elementId: ''
    showDate: true
    showAuthor: false
    showExcerpt: true
    showReadMoreLink: true
    readMoreLinkLabel: View more
    actions:
      - type: Link
        label: See all adventures
        altText: See all adventures
        url: /blog
        showIcon: true
        icon: arrowRight
    styles:
      self:
        height: auto
        width: wide
        padding:
          - pt-24
          - pb-24
          - pl-4
          - pr-4
        justifyContent: center
      title:
        textAlign: left
      subtitle:
        textAlign: left
      actions:
        justifyContent: flex-start
    title: Seasonal adventure
    subtitle: ''
    posts:
      - content/pages/blog/post-five.md
      - content/pages/blog/post-three.md
metaDescription: null
socialImage: null
author: content/data/team/hilary-ouse.json
---
I worked on this project post Covid-19 pandemic, and was inspired to work on this topic, because of what was happening around us. I wanted to learn more about mental health, causes and factors. 

Mental health is a significant concern in the United States, affecting nearly 500 million adults. Various factors, including genetics, traumatic events, physical health, and societal issues, contribute to mental health challenges. 

Linear Probability Models indicated that the overall impact of region on mental health was not statistically significant. However, Logit Models revealed significant differences between regions. North Central/Midwest and South regions showed a negative impact on mental health compared to the Northeast, with varying significance levels. The models also explored differences based on marital status, suggesting that location has a more significant impact on the mental health of single individuals compared to married individuals.

The study concludes that there is a significant relationship between region and mental health in the United States. Future research should incorporate additional control variables such as weather and migration patterns to further understand the complexities of this relationship. The study provides valuable insights for policymakers and individuals seeking ways to improve mental well-being, suggesting that regional relocation could be a viable option.

The complete paper can be accessed at the following link: 

[https://drive.google.com/file/d/1jkkXODXSw9-2-P6rs4raFwO9nzVxGS4E/view?usp=sharing](https://drive.google.com/file/d/1jkkXODXSw9-2-P6rs4raFwO9nzVxGS4E/view?usp=sharingThank)

Thank you

