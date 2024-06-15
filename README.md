
Quartz can generate a list of recent notes based on some filtering and sorting criteria. Though this component isn't included in any [[layout]] by default, you can add it by using `Component.RecentNotes` in `quartz.layout.ts`.

## Customization

- Changing the title from "Recent notes": pass in an additional parameter to `Component.RecentNotes({ title: "Recent writing" })`
- Changing the number of recent notes: pass in an additional parameter to `Component.RecentNotes({ limit: 5 })`
- Display the note's tags (defaults to true): `Component.RecentNotes({ showTags: false })`
- Show a 'see more' link: pass in an additional parameter to `Component.RecentNotes({ linkToMore: "tags/components" })`. This field should be a full slug to a page that exists.
- Customize filtering: pass in an additional parameter to `Component.RecentNotes({ filter: someFilterFunction })`. The filter function should be a function that has the signature `(f: QuartzPluginData) => boolean`.
- Customize sorting: pass in an additional parameter to `Component.RecentNotes({ sort: someSortFunction })`. By default, Quartz will sort by date and then tie break lexographically. The sort function should be a function that has the signature `(f1: QuartzPluginData, f2: QuartzPluginData) => number`. See `byDateAndAlphabetical` in `quartz/components/PageList.tsx` for an example.
- Component: `quartz/components/RecentNotes.tsx`
- Style: `quartz/components/styles/recentNotes.scss`
# Quartz v4

> “[One] who works with the door open gets all kinds of interruptions, but [they] also occasionally gets clues as to what the world is and what might be important.” — Richard Hamming

Quartz is a set of tools that helps you publish your [digital garden](https://jzhao.xyz/posts/networked-thought) and notes as a website for free.
Quartz v4 features a from-the-ground rewrite focusing on end-user extensibility and ease-of-use.

🔗 Read the documentation and get started: https://quartz.jzhao.xyz/

[Join the Discord Community](https://discord.gg/cRFFHYye7t)

## Sponsors

<p align="center">
  <a href="https://github.com/sponsors/jackyzha0">
    <img src="https://cdn.jsdelivr.net/gh/jackyzha0/jackyzha0/sponsorkit/sponsors.svg" />
  </a>
</p>
