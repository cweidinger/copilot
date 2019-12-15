# Schema

At Copilot, we thoroughly believe that the data you put into our app is yours and that you should have meaningful export access to it. In addition to the export functionality, the following explanations of types should help you interpret your exported data if you'd like to import it into a different system or just analyze it yourself ;).

## Overview

- SyncItem (item) - A singular piece of data that has a unique $key.
- Repository ($repo) - A store of data. Each user has their personal repo which cannot be shared. Additional repos can be created that can be shared (this feature is currently disabled to new users).
- Type ($type)- A signal to the app to present your data in certain ways in the app.
- Relationships - A connection between individual items.

## Types

- Input
- Note
- Routine
- Time Log Account
  - Time Log Entry
- Goal
  - Project
    - Action
- Store
  - Item (text entry and upc)

## Types with limited support

- Checklist
  - Checklist Item
- Media - This is a feature, not a type.
  - Book
  - Audiobook, Hoopla
  - Link
- Playlist
- Tag
  - Place
  - Person
  - People - a grouping of persons
  - Timeframes
- View, Feature View - These types are how information associated with your views in the app are stored.
- Bookmark

### Detail Types

- Metric - Timeseries data associated with a type.
- Text - In the future text will be stored independently of the reference to the text so this type is a placeholder for that future feature.
- UPC Purchase - A purchase event of a product.

## Relationships

- blocks, blockedBy - An item that is blocked by another item means that it cannot be started until the blocking item is done.
- tags, taggedBy - These associate any type to any other type with a generic relationship.
- impls, impledBy - Implements means that doing one thing is part of doing a bigger thing. Like an action is part of doing a project.
- bookmarks, bookmarkedBy - All bookmarked items appear in the bookmarked list. Bookmarks can be sorted independently of the items that they reference.
- hasChecklistItem, isOnChecklist - A legacy special type for the relationship between Checklist and Checklist Items which will eventually be replaced by Impls and Impled By.
- lastFeatureView - This keeps track of where you were last in the app so that when the app reloads, you don't lose your place.
