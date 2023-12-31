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
title: 'SQL: Bike Retail Store'
colors: colors-d
date: '2022-12-02'
featuredImage:
  type: ImageBlock
  url: /images/Screen Shot 2023-02-11 at 6.25.24 PM.png
  altText: Post Image
media:
  type: ImageBlock
  altText: Post Image
  url: /images/Screen Shot 2023-02-11 at 6.25.24 PM.png
bottomSections:
  - elementId: ''
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
  - type: HeroSection
    colors: colors-d
    elementId: ''
    backgroundSize: full
    title: We do fishing differently
    subtitle: Fresh. Better. Faster.
    text: ''
    actions:
      - type: Button
        label: Join adventure
        showIcon: true
        icon: arrowRight
        style: primary
        url: /
    media:
      type: ImageBlock
      url: /images/hero-2.png
      altText: Hero image
    backgroundImage: null
    styles:
      self:
        height: auto
        width: wide
        padding:
          - pt-36
          - pb-48
          - pl-4
          - pr-4
        alignItems: center
        justifyContent: center
        flexDirection: row
      title:
        textAlign: left
      subtitle:
        textAlign: left
      text:
        textAlign: left
      actions:
        justifyContent: flex-start
metaDescription: null
socialImage: null
author: content/data/team/hugh-saturation.json
---
For this project, we used SQL to see the overall performance of a fictional bicycle store and its products. After data cleaning and mining, we were able to to see patterns which helped us create tables and visualizations representing areas of production, consumers, and sales.

Working on this project strengthened my skills in: writing SQL scripts, connecting tables and creating relationships, and visualizations. The link to this project can be found below.

<https://docs.google.com/presentation/d/1asYMIqRAAp2lzxLHUYhCSk1ipLFwZ4Lq/edit?usp=sharing&ouid=104430033042466969075&rtpof=true&sd=true>

>

