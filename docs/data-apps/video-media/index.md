---
title: "Video and Media Analytics"
sidebar_position: 5
sidebar_label: "Video and Media Analytics"
---

:::caution

This data app is currently in Public Preview and features may change without notice.

:::

While 91% of businesses use video as a marketing tool, few businesses deeply understand how their users interact with this content and what effect this has on business metrics. Collecting vital engagement data plays a significant role in understanding your audience, optimizing your content, and measuring the impact of your video and media marketing efforts.

Our **Video and Media Analytics** app helps you visualize insights on your video, audio and streaming content, based on data generated by our media plugins and [Media Player DBT package](docs/modeling-your-data/modeling-your-data-with-dbt/dbt-models/dbt-media-player-data-model/index.md). It comes with the following dashboards:

1. **Overview**: Get a high-level view across all your media and video content performance including 'total watch time', 'plays over time', and 'top-performing content'.
2. **Content**: Dive deeper into individual media items through an impression to plays funnel, audience retention chart and views over time graph.
3. **In-Media Ads**: Improve advertising performance with key metrics like 'click-through-rate' and see what content returned the most ad views and clicks. Know how far viewers reach through your ads with the Ad Audience Retention chart, to understand where in the ad viewers may be skipping to improve ad creative performance.

### Requirements

- Running the [Snowplow Media dbt Package](docs/modeling-your-data/modeling-your-data-with-dbt/dbt-models/dbt-media-player-data-model/index.md)
- Access to the derived tables granted to the role used when setting up the data app
- Media events tracked using the media plugins for the [JavaScript](/docs/collecting-data/collecting-from-own-applications/javascript-trackers/web-tracker/tracking-events/media/index.md) or [mobile trackers](/docs/collecting-data/collecting-from-own-applications/mobile-trackers/tracking-events/media-tracking/index.md). Note that there are multiple JavaScript tracker media plugins available. Implementation of a v2 plugin is required for this data app to work as intended.

## Usage

The following steps will guide you through using the app.

### Step 1: Configure using the Media dbt package tables

The **Settings** page lets you choose the schema and tables in your data warehouse to use in the app.
These refer to the output of the Media dbt package.

First, choose the warehouse schema where your dbt Media package produced the derived tables (e.g., `dbt_media_derived`).
The app will suggest the most likely tables.
The following derived tables will need to be configured: `base`, and `ad views` tables.

Verify that these match the desired tables and click "Save Settings".
The app will then check that the tables have the required columns.
If successful, you can navigate to the dashboard pages in the sidebar and explore your data.

### Step 2: Explore the dashboards

You can browse the following pages:

1. **Overview** shows the key metrics across all media, including number of plays, average play time, and number of unique viewers. It also shows a table with details and metrics for all media items.
2. **Content** dives deeper into the individual media items. Choose one piece of media to see metrics such as total plays and total watch time, as well as charts for plays over time by platform, an engagement funnel, and retention across the media playtime.
3. **In-Media Ads** shows engagement with ads, including impressions over time, clicks, and clickthrough rate.

### Step 3: Choose the date range and filters

At the top of each page, there is an option to choose the date range. The Content and In-Media Ads pages also have filters for individual items of media. These options let you narrow down the data shown in the dashboard to what you are interested in.