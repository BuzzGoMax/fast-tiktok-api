[Fast Tiktok API](https://apify.com/novi/fast-tiktok-api?fpr=data)

## Introduction

This is a **powerful TikTok video scraper** that allows you to extract various types of data from TikTok, such as video
lists by trend, hashtag, user, search, and music. It also provides the ability to retrieve video information by URL and
obtain comment lists by video.
For just $0.001, you can obtain up to 100 results.

Say goodbye to watermarked videos as our data **provides the URL without watermarks**.
**No proxy needed, you can save hundreds USD a month!**

**Note:** If you need an Actor with business scale, lease try this actor: [**Ultimate TikTok Scraper**](https://apify.com/novi/tiktok-scraper-ultimate?fpr=7hce1m).

## Features

- Get video lists by trend, hashtag, user, search, and music.
- Retrieve video information by URL.
- Extract comment lists by video.
- Supports multiple programming languages via the APIFY SDK or RESTful API.
- No additional dependencies or libraries required.
- Compatible with various programming languages through the APIFY SDK or RESTful API.
- Accessible via API keys or RESTful API calls.
- Works with any programming language.
- Extracts public data only, ensuring privacy and compliance.

## Documentation

[Video](https://www.youtube.com/embed/5SfmiNLCGRM?enablejsapi=1&rel=0)

For detailed information on how to use the **Fast TikTok API Scraper**, please refer to
the [official documentation](https://docs.apify.com/platform/actors/running). The documentation provides a user guide,
API reference, and examples to help you get started.

UI Input Page
Tutorial: [Fast TikTok API: The Complete Guide to All Scraping Types](https://novidevelop.github.io/tiktok/api/tutorial/data-extraction/guide/2025/03/10/fast-tiktok-api-input-guide-complation.html).

A tutorial blog for coding can be found
at [Download Trending TikTok Videos Easily with Fast TikTok API](https://novidevelop.github.io/tiktok/scraper/2025/02/23/download-trending-tiktok-videos-easily-with-fast-tiktok-api.html).

✨🚀⭐💡**New Version:** [Tiktok Scraper Ultimate (pay-per-event)](https://apify.com/novi/tiktok-scraper-ultimate?fpr=7hce1m)

## Support

If you encounter any issues or have questions about the scraper, you can seek support through the Apify actor issue
tracker or join the Apify Discord server for community support.

## Bugs, fixes, updates and changelog

Stay updated with the latest bug fixes, updates, and changelog as this scraper undergoes active development.

Enjoy optimized performance, as the actor is designed to scrape numerous listings with minimal memory consumption. It
can crawl 100 items using only 128MB of memory.

## Input Parameters

The input of this scraper should be JSON containing the list of pages on Fast TikTok API that should be visited.
Required fields are:

| **FIELD** | **Type** | **Description** |
| --- | --- | --- |
| type | string | Scrapping Type: SEARCH, TREND, HASHTAG, USER, MUSIC, VIDEO |
| url | string | URL correspond to type. Use when Type is HASHTAG, USER, MUSIC |
| urls | string[] | Video URLs. Use when Type is VIDEO.  Ex: [https://www.tiktok.com/@seuamigopitbull/video/7137451371405561093](https://www.tiktok.com/@seuamigopitbull/video/7137451371405561093) |
| region | string | 2 characters region code. Ex: US. Use when Type is TREND, SEARCH |
| keyword | String | Keyword to scrap |
| limit | integer | You can limit scraped results. |
| isUnlimited | boolean | Get all if possible |
| sortType | integer | Sort Type. Use when Type is SEARCH. 0: Relevance. 1: Most liked. 2: Most recent |
| publishTime | string | Publish Time. Use when Type is SEARCH. |
| isDownloadVideoCover | boolean | Download Cover Image |
| isDownloadVideo | boolean | Download Video (no watermark) |
| **`customMapFunction`** | String | (Advanced) Lets you write a bit of JavaScript code to change the output data for every single item. |

## Compute Unit Consumption

**The Fast TikTok API** actor is optimized for blazing-fast performance, allowing it to scrape up to 1000 listings in
just 60 seconds with approximately $0.004.

## Fast TikTok API Input example

**SEARCH**

```
{
  "type": "SEARCH",
  "keyword": "viral",
  "sortType": 0,
  "publishTime": "ALL_TIME",
  "limit": 100,
  "isUnlimited": false
}
```

**TREND**

```
{
  "type": "TREND",
  "region": "US",
  "limit": 100,
  "isUnlimited": false
}
```

**HASHTAG**

```
{
  "type": "HASHTAG",
  "url": "https://www.tiktok.com/tag/fyp",
  "limit": 100,
  "isUnlimited": false
}
```

**VIDEO**

```
{
  "type": "VIDEO",
  "urls": [
    "https://www.tiktok.com/@seuamigopitbull/video/7137451371405561093",
    "https://www.tiktok.com/@scarymanilla/video/7023014317612207366"
  ]
}
```

**MUSIC**

```
{
  "type": "MUSIC",
  "url": "https://www.tiktok.com/music/original-sound-7023014141862808326",
  "limit": 100,
  "isUnlimited": false
}
```

## During the Run

Receive informative messages throughout the process, providing insights into the current page being processed and the
number of loaded items.

In case of incorrect input, the actor will immediately stop and provide an explanation of the error.

## Fast TikTok API Export

Results obtained during the run are stored in a dataset, with each item as a separate entry. Easily manage and access
the results in your preferred programming language, such as Python, PHP, or Node JS/NPM. Refer to our FAQ or API
references for more details on retrieving results from the Fast TikTok API actor.

### Video Item Detail

```
[
  {
    "added_sound_music_info": {
      "album": "",
      "artists": [],
      "audition_duration": 54,
      "author": "VTV Giai Tri Official",
      "author_deleted": false,
      "author_position": null,
      "avatar_medium": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=Nq4qV8EaKGCuXuy1BNauD7klTH0%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=x8tIQWWiY3wzNiefIUjhh8g9q9o%3D"
        ],
        "width": 720
      },
      "avatar_thumb": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=FHXsU3jZ8YKoyxCWYxnwF3W3o2w%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=AbJ3SuoZHmlN4DCbqkYoVmpbci8%3D"
        ],
        "width": 720
      },
      "binded_challenge_id": 0,
      "can_not_reuse": false,
      "collect_stat": 0,
      "commercial_right_type": 2,
      "cover_large": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/1080x1080/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=y9%2Fv5Fnzgc6JHvd%2Fu7gW2Pvz6L4%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/1080x1080/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=7FvoANBrpBQ6BeEnRWZzFg8gCHY%3D"
        ],
        "width": 720
      },
      "cover_medium": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=Nq4qV8EaKGCuXuy1BNauD7klTH0%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=x8tIQWWiY3wzNiefIUjhh8g9q9o%3D"
        ],
        "width": 720
      },
      "cover_thumb": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=FHXsU3jZ8YKoyxCWYxnwF3W3o2w%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=AbJ3SuoZHmlN4DCbqkYoVmpbci8%3D"
        ],
        "width": 720
      },
      "dmv_auto_show": false,
      "duration": 54,
      "duration_high_precision": {
        "audition_duration_precision": 54.7,
        "duration_precision": 54.7,
        "shoot_duration_precision": 54.7,
        "video_duration_precision": 54.7
      },
      "external_song_info": [],
      "extra": "{\"aed_music_dur\":1,\"beats\":{},\"can_read\":true,\"can_reuse\":true,\"erase_type\":0,\"erase_uid\":0,\"from_user_id\":0,\"has_edited\":0,\"is_ugc_mapping\":false,\"is_used\":0,\"owner_id\":6812490744957256705,\"resource_status\":0,\"review_unshelve_reason\":0,\"reviewed\":0,\"schedule_search_time\":0}",
      "id": 7229168247013182210,
      "id_str": "7229168247013182210",
      "is_audio_url_with_cookie": false,
      "is_author_artist": false,
      "is_commerce_music": true,
      "is_matched_metadata": false,
      "is_original": false,
      "is_original_sound": true,
      "is_pgc": false,
      "is_play_music": false,
      "is_shooting_allow": true,
      "lyric_short_position": null,
      "mid": "7229168247013182210",
      "multi_bit_rate_play_info": null,
      "mute_share": false,
      "offline_desc": "",
      "owner_handle": "vtvgiaitriofficial",
      "owner_id": "6812490744957256705",
      "owner_nickname": "VTV Giai Tri Official",
      "play_url": {
        "height": 720,
        "uri": "https://sf16-ies-music-sg.tiktokcdn.com/obj/tiktok-obj/7229168238650166018.mp3",
        "url_list": [
          "https://sf16-ies-music-sg.tiktokcdn.com/obj/tiktok-obj/7229168238650166018.mp3"
        ],
        "width": 720
      },
      "position": null,
      "prevent_download": false,
      "preview_end_time": 0,
      "preview_start_time": 0,
      "recommend_status": 100,
      "search_highlight": null,
      "sec_uid": "MS4wLjABAAAAcmWx88_xRFU57rY2YUYFPBarAgam7vOnfxR-TvpyfvKtkFEAsihLpdILoRLvqYjV",
      "shoot_duration": 54,
      "source_platform": 24,
      "status": 1,
      "tag_list": null,
      "title": "original sound - vtvgiaitriofficial",
      "tt_to_dsp_song_infos": null,
      "user_count": 0,
      "video_duration": 54
    },
    "anchors": null,
    "anchors_extras": "",
    "author": {
      "accept_private_policy": false,
      "account_labels": null,
      "account_region": "",
      "ad_cover_url": null,
      "advance_feature_item_order": null,
      "advanced_feature_info": null,
      "apple_account": 0,
      "authority_status": 0,
      "avatar_168x168": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d~c5_168x168.webp?x-expires=1683439200&x-signature=EZgY2zBsY%2FsguEcz5u9%2FZsZ78f8%3D",
          "https://p16-sign-sg.tiktokcdn.com/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d~c5_168x168.jpeg?x-expires=1683439200&x-signature=pYatTidlUIwOx%2Bf6w99kydOl%2Fss%3D"
        ],
        "width": 720
      },
      "avatar_300x300": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d~c5_300x300.webp?x-expires=1683439200&x-signature=8%2BSgQSGrkVrU9GhImQQMSDnKu5w%3D",
          "https://p16-sign-sg.tiktokcdn.com/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d~c5_300x300.jpeg?x-expires=1683439200&x-signature=Dpu9ST3GbZxtmhGvEWXtOQG7VX4%3D"
        ],
        "width": 720
      },
      "avatar_larger": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/1080x1080/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=y9%2Fv5Fnzgc6JHvd%2Fu7gW2Pvz6L4%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/1080x1080/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=7FvoANBrpBQ6BeEnRWZzFg8gCHY%3D"
        ],
        "width": 720
      },
      "avatar_medium": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=Nq4qV8EaKGCuXuy1BNauD7klTH0%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=x8tIQWWiY3wzNiefIUjhh8g9q9o%3D"
        ],
        "width": 720
      },
      "avatar_thumb": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=FHXsU3jZ8YKoyxCWYxnwF3W3o2w%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=AbJ3SuoZHmlN4DCbqkYoVmpbci8%3D"
        ],
        "width": 720
      },
      "avatar_uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
      "aweme_count": 0,
      "bind_phone": "",
      "bold_fields": null,
      "can_message_follow_status_list": null,
      "can_set_geofencing": null,
      "cha_list": null,
      "comment_filter_status": 1,
      "comment_setting": 0,
      "commerce_user_level": 0,
      "cover_url": [
        {
          "height": 720,
          "uri": "musically-maliva-obj/1612555907887110",
          "url_list": [
            "https://p16-amd-va.tiktokcdn.com/obj/musically-maliva-obj/1612555907887110"
          ],
          "width": 720
        }
      ],
      "create_time": 0,
      "custom_verify": "Verified account",
      "cv_level": "",
      "download_prompt_ts": 0,
      "download_setting": 3,
      "duet_setting": 0,
      "enterprise_verify_reason": "",
      "events": null,
      "favoriting_count": 0,
      "fb_expire_time": 0,
      "follow_status": 0,
      "follower_count": 0,
      "follower_status": 0,
      "followers_detail": null,
      "following_count": 0,
      "friends_status": 0,
      "gender": 0,
      "geofencing": null,
      "google_account": "",
      "has_email": false,
      "has_facebook_token": false,
      "has_insights": false,
      "has_orders": false,
      "has_twitter_token": false,
      "has_youtube_token": false,
      "hide_search": false,
      "homepage_bottom_toast": null,
      "ins_id": "",
      "is_ad_fake": false,
      "is_block": false,
      "is_discipline_member": false,
      "is_phone_binded": false,
      "is_star": false,
      "item_list": null,
      "language": "en",
      "live_agreement": 0,
      "live_commerce": false,
      "live_verify": 0,
      "mention_status": 1,
      "mutual_relation_avatars": null,
      "need_points": null,
      "need_recommend": 0,
      "nickname": "VTV Giai Tri Official",
      "platform_sync_info": null,
      "prevent_download": false,
      "react_setting": 0,
      "region": "VN",
      "relative_users": null,
      "room_id": 0,
      "search_highlight": null,
      "sec_uid": "MS4wLjABAAAAcmWx88_xRFU57rY2YUYFPBarAgam7vOnfxR-TvpyfvKtkFEAsihLpdILoRLvqYjV",
      "secret": 0,
      "share_info": {
        "now_invitation_card_image_urls": null,
        "share_desc": "",
        "share_desc_info": "",
        "share_qrcode_url": {
          "height": 720,
          "uri": "",
          "url_list": [],
          "width": 720
        },
        "share_title": "",
        "share_title_myself": "",
        "share_title_other": "",
        "share_url": ""
      },
      "share_qrcode_uri": "",
      "shield_comment_notice": 0,
      "shield_digg_notice": 0,
      "shield_edit_field_info": null,
      "shield_follow_notice": 0,
      "short_id": "0",
      "show_image_bubble": false,
      "signature": "Mời các bạn tải ứng dụng VTV GiảiTrí để xem trọn bộ phim hay độc quyền",
      "special_account": {
        "special_account_list": null
      },
      "special_lock": 1,
      "status": 1,
      "stitch_setting": 0,
      "total_favorited": 0,
      "tw_expire_time": 0,
      "twitter_id": "",
      "twitter_name": "",
      "type_label": null,
      "uid": "6812490744957256705",
      "unique_id": "vtvgiaitriofficial",
      "unique_id_modify_time": 1683353131,
      "user_canceled": false,
      "user_mode": 1,
      "user_period": 0,
      "user_profile_guide": null,
      "user_rate": 1,
      "user_tags": null,
      "verification_type": 0,
      "verify_info": "",
      "video_icon": {
        "height": 720,
        "uri": "",
        "url_list": [],
        "width": 720
      },
      "white_cover_url": null,
      "with_commerce_entry": false,
      "with_shop_entry": false,
      "youtube_channel_id": "UCuJ5k3GndbHnXLYyiIR6Z8Q",
      "youtube_channel_title": "VTV Giải Trí Official",
      "youtube_expire_time": 0
    },
    "author_user_id": 6812490744957256705,
    "aweme_acl": {
      "download_general": {
        "code": 1,
        "extra": "101",
        "mute": false,
        "show_type": 0,
        "transcode": 1
      },
      "download_mask_panel": {
        "code": 1,
        "extra": "101",
        "mute": false,
        "show_type": 0,
        "transcode": 1
      },
      "platform_list": null,
      "share_general": {
        "code": 1,
        "extra": "101",
        "mute": false,
        "show_type": 1,
        "toast_msg": "This action isn't allowed for this post",
        "transcode": 1
      },
      "share_list_status": 0
    },
    "aweme_id": "7229167805625847041",
    "aweme_type": 0,
    "behind_the_song_music_ids": null,
    "behind_the_song_video_music_ids": null,
    "bodydance_score": 0,
    "branded_content_accounts": null,
    "cc_template_info": {
      "author_name": "",
      "clip_count": 0,
      "desc": "",
      "duration_milliseconds": 0,
      "related_music_id": "",
      "template_id": ""
    },
    "cha_list": [
      {
        "author": {
          "account_labels": null,
          "ad_cover_url": null,
          "advance_feature_item_order": null,
          "advanced_feature_info": null,
          "bold_fields": null,
          "can_message_follow_status_list": null,
          "can_set_geofencing": null,
          "cha_list": null,
          "cover_url": null,
          "events": null,
          "followers_detail": null,
          "geofencing": null,
          "homepage_bottom_toast": null,
          "item_list": null,
          "mutual_relation_avatars": null,
          "need_points": null,
          "platform_sync_info": null,
          "relative_users": null,
          "search_highlight": null,
          "shield_edit_field_info": null,
          "type_label": null,
          "user_profile_guide": null,
          "user_tags": null,
          "white_cover_url": null
        },
        "banner_list": null,
        "cha_attrs": null,
        "cha_name": "cuocdoivandepsao",
        "cid": "1670903934915585",
        "collect_stat": 0,
        "connect_music": [],
        "desc": "",
        "extra_attr": {
          "is_live": false
        },
        "hashtag_profile": "",
        "is_challenge": 0,
        "is_commerce": false,
        "is_pgcshow": false,
        "schema": "aweme://aweme/challenge/detail?cid=1670903934915585",
        "search_highlight": null,
        "share_info": {
          "bool_persist": 0,
          "now_invitation_card_image_urls": null,
          "share_desc": "Check out #cuocdoivandepsao on TikTok!",
          "share_desc_info": "Check out #cuocdoivandepsao on TikTok!",
          "share_quote": "",
          "share_signature_desc": "",
          "share_signature_url": "",
          "share_title": "It is a becoming a big trend on TikTok now! Click here: cuocdoivandepsao",
          "share_title_myself": "",
          "share_title_other": "",
          "share_url": "https://www.tiktok.com/tag/cuocdoivandepsao?_r=1&name=cuocdoivandepsao&u_code=0&_d=e7km4e8ee8j7d2&share_challenge_id=1670903934915585&sharer_language=en&source=h5_m"
        },
        "show_items": null,
        "sub_type": 0,
        "type": 1,
        "use_count": 0,
        "user_count": 0,
        "view_count": 0
      }
    ],
    "challenge_position": null,
    "cmt_swt": false,
    "collect_stat": 0,
    "commerce_config_data": null,
    "commerce_info": {
      "adv_promotable": false,
      "auction_ad_invited": false,
      "with_comment_filter_words": false
    },
    "content_desc": "",
    "content_desc_extra": [],
    "cover_labels": null,
    "create_time": 1683171893,
    "desc": "Cô chủ trọ cho thuê căn phòng hết nước chấm thật #Cuocdoivandepsao",
    "desc_language": "vi",
    "disable_search_trending_bar": false,
    "distance": "",
    "distribute_type": 1,
    "follow_up_publish_from_id": 0,
    "geofencing": null,
    "geofencing_regions": null,
    "green_screen_materials": null,
    "group_id": "7228596161530039558",
    "group_id_list": {
      "GroupdIdList0": null,
      "GroupdIdList1": null
    },
    "has_vs_entry": false,
    "have_dashboard": false,
    "hybrid_label": null,
    "image_infos": null,
    "interact_permission": {
      "allow_adding_to_story": 1,
      "allow_create_sticker": {
        "status": 0
      },
      "duet": 0,
      "duet_privacy_setting": 0,
      "stitch": 0,
      "stitch_privacy_setting": 0,
      "upvote": 0
    },
    "interaction_stickers": null,
    "is_ads": false,
    "is_description_translatable": true,
    "is_hash_tag": 1,
    "is_on_this_day": 0,
    "is_pgcshow": false,
    "is_preview": 0,
    "is_relieve": false,
    "is_text_sticker_translatable": false,
    "is_top": 0,
    "is_vr": false,
    "item_comment_settings": 0,
    "item_duet": 0,
    "item_react": 0,
    "item_stitch": 0,
    "label_top": {
      "height": 720,
      "uri": "tiktok-obj/1598708589477025.PNG",
      "url_list": [
        "https://p16-sg.tiktokcdn.com/obj/tiktok-obj/1598708589477025.PNG"
      ],
      "width": 720
    },
    "label_top_text": null,
    "long_video": null,
    "mask_infos": [],
    "misc_info": "{}",
    "muf_comment_info_v2": null,
    "music": {
      "album": "",
      "artists": [],
      "audition_duration": 54,
      "author": "VTV Giai Tri Official",
      "author_deleted": false,
      "author_position": null,
      "avatar_medium": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=Nq4qV8EaKGCuXuy1BNauD7klTH0%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=x8tIQWWiY3wzNiefIUjhh8g9q9o%3D"
        ],
        "width": 720
      },
      "avatar_thumb": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=FHXsU3jZ8YKoyxCWYxnwF3W3o2w%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=AbJ3SuoZHmlN4DCbqkYoVmpbci8%3D"
        ],
        "width": 720
      },
      "binded_challenge_id": 0,
      "can_not_reuse": false,
      "collect_stat": 0,
      "commercial_right_type": 2,
      "cover_large": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/1080x1080/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=y9%2Fv5Fnzgc6JHvd%2Fu7gW2Pvz6L4%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/1080x1080/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=7FvoANBrpBQ6BeEnRWZzFg8gCHY%3D"
        ],
        "width": 720
      },
      "cover_medium": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=Nq4qV8EaKGCuXuy1BNauD7klTH0%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/720x720/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=x8tIQWWiY3wzNiefIUjhh8g9q9o%3D"
        ],
        "width": 720
      },
      "cover_thumb": {
        "height": 720,
        "uri": "tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.webp?x-expires=1683439200&x-signature=FHXsU3jZ8YKoyxCWYxnwF3W3o2w%3D",
          "https://p16-sign-sg.tiktokcdn.com/aweme/100x100/tos-alisg-avt-0068/e58bf19abf1c1badb25233ebb772283d.jpeg?x-expires=1683439200&x-signature=AbJ3SuoZHmlN4DCbqkYoVmpbci8%3D"
        ],
        "width": 720
      },
      "dmv_auto_show": false,
      "duration": 54,
      "duration_high_precision": {
        "audition_duration_precision": 54.7,
        "duration_precision": 54.7,
        "shoot_duration_precision": 54.7,
        "video_duration_precision": 54.7
      },
      "external_song_info": [],
      "extra": "{\"aed_music_dur\":1,\"beats\":{},\"can_read\":true,\"can_reuse\":true,\"erase_type\":0,\"erase_uid\":0,\"from_user_id\":0,\"has_edited\":0,\"is_ugc_mapping\":false,\"is_used\":0,\"owner_id\":6812490744957256705,\"resource_status\":0,\"review_unshelve_reason\":0,\"reviewed\":0,\"schedule_search_time\":0}",
      "id": 7229168247013182210,
      "id_str": "7229168247013182210",
      "is_audio_url_with_cookie": false,
      "is_author_artist": false,
      "is_commerce_music": true,
      "is_matched_metadata": false,
      "is_original": false,
      "is_original_sound": true,
      "is_pgc": false,
      "is_play_music": false,
      "is_shooting_allow": true,
      "lyric_short_position": null,
      "mid": "7229168247013182210",
      "multi_bit_rate_play_info": null,
      "mute_share": false,
      "offline_desc": "",
      "owner_handle": "vtvgiaitriofficial",
      "owner_id": "6812490744957256705",
      "owner_nickname": "VTV Giai Tri Official",
      "play_url": {
        "height": 720,
        "uri": "https://sf16-ies-music-sg.tiktokcdn.com/obj/tiktok-obj/7229168238650166018.mp3",
        "url_list": [
          "https://sf16-ies-music-sg.tiktokcdn.com/obj/tiktok-obj/7229168238650166018.mp3"
        ],
        "width": 720
      },
      "position": null,
      "prevent_download": false,
      "preview_end_time": 0,
      "preview_start_time": 0,
      "recommend_status": 100,
      "search_highlight": null,
      "sec_uid": "MS4wLjABAAAAcmWx88_xRFU57rY2YUYFPBarAgam7vOnfxR-TvpyfvKtkFEAsihLpdILoRLvqYjV",
      "shoot_duration": 54,
      "source_platform": 24,
      "status": 1,
      "tag_list": null,
      "title": "original sound - vtvgiaitriofficial",
      "tt_to_dsp_song_infos": null,
      "user_count": 0,
      "video_duration": 54
    },
    "music_begin_time_in_ms": 0,
    "music_selected_from": "",
    "music_title_style": 1,
    "need_trim_step": false,
    "need_vs_entry": false,
    "nickname_position": null,
    "no_selected_music": false,
    "origin_comment_ids": null,
    "playlist_blocked": false,
    "playlist_info": {
      "index": 6,
      "item_total": 43,
      "mix_id": "7220755092813777691",
      "name": "Cuộc đời vẫn đẹp sao"
    },
    "poi_re_tag_signal": 0,
    "position": null,
    "prevent_download": false,
    "products_info": null,
    "question_list": null,
    "rate": 12,
    "reference_tts_voice_ids": null,
    "reference_voice_filter_ids": null,
    "region": "VN",
    "risk_infos": {
      "content": "",
      "risk_sink": false,
      "type": 0,
      "vote": false,
      "warn": false
    },
    "search_highlight": null,
    "share_info": {
      "bool_persist": 0,
      "now_invitation_card_image_urls": null,
      "share_desc": "Check out VTV Giai Tri Official's video! #TikTok",
      "share_desc_info": "TikTok: Make Every Second CountCheck out VTV Giai Tri Official’s video! #TikTok > ",
      "share_link_desc": "",
      "share_quote": "",
      "share_signature_desc": "",
      "share_signature_url": "",
      "share_title": "Check out VTV Giai Tri Official’s video! #TikTok > ",
      "share_title_myself": "",
      "share_title_other": "",
      "share_url": "https://www.tiktok.com/@vtvgiaitriofficial/video/7229167805625847041?_r=1&u_code=0&preview_pb=0&sharer_language=en&_d=e7km4e8ee8j7d2&share_item_id=7229167805625847041&source=h5_m",
      "whatsapp_desc": "Download TikTok and watch more fun videos:"
    },
    "share_url": "https://www.tiktok.com/@vtvgiaitriofficial/video/7229167805625847041?_r=1&u_code=0&preview_pb=0&sharer_language=en&_d=e7km4e8ee8j7d2&share_item_id=7229167805625847041&source=h5_m",
    "sort_label": "",
    "statistics": {
      "aweme_id": "7229167805625847041",
      "collect_count": 743,
      "comment_count": 183,
      "digg_count": 25006,
      "download_count": 0,
      "forward_count": 0,
      "lose_comment_count": 0,
      "lose_count": 0,
      "play_count": 585709,
      "share_count": 492,
      "whatsapp_share_count": 0
    },
    "status": {
      "allow_comment": true,
      "allow_share": true,
      "aweme_id": "7229167805625847041",
      "download_status": 0,
      "in_reviewing": false,
      "is_delete": false,
      "is_prohibited": false,
      "private_status": 0,
      "review_result": {
        "review_status": 0
      },
      "reviewed": 1,
      "self_see": false
    },
    "text_extra": [
      {
        "end": 66,
        "hashtag_id": "1670903934915585",
        "hashtag_name": "cuocdoivandepsao",
        "is_commerce": false,
        "sec_uid": "",
        "start": 49,
        "type": 1,
        "user_id": ""
      }
    ],
    "text_sticker_major_lang": "un",
    "tts_voice_ids": null,
    "uniqid_position": null,
    "user_digged": 0,
    "video": {
      "CoverTsp": 47,
      "ai_dynamic_cover": {
        "uri": "tos-alisg-p-0037/ad27d3bd0b00480d860c9e22f87b3ac5_1683171895",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/ad27d3bd0b00480d860c9e22f87b3ac5_1683171895?x-expires=1683439200&x-signature=8Dfb9ZLKsy0h2BMmAKuEOpwyl7w%3D&s=CHALLENGE_AWEME&se=false&sh=&sc=dynamic_cover&l=20230506060531760EDB96FF74C50AB8A9"
        ]
      },
      "ai_dynamic_cover_bak": {
        "uri": "tos-alisg-p-0037/ad27d3bd0b00480d860c9e22f87b3ac5_1683171895",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/ad27d3bd0b00480d860c9e22f87b3ac5_1683171895?x-expires=1683439200&x-signature=8Dfb9ZLKsy0h2BMmAKuEOpwyl7w%3D&s=CHALLENGE_AWEME&se=false&sh=&sc=dynamic_cover&l=20230506060531760EDB96FF74C50AB8A9"
        ]
      },
      "animated_cover": {
        "uri": "tos-alisg-p-0037/ad27d3bd0b00480d860c9e22f87b3ac5_1683171895",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/ad27d3bd0b00480d860c9e22f87b3ac5_1683171895?x-expires=1683439200&x-signature=8Dfb9ZLKsy0h2BMmAKuEOpwyl7w%3D&s=CHALLENGE_AWEME&se=false&sh=&sc=dynamic_cover&l=20230506060531760EDB96FF74C50AB8A9"
        ]
      },
      "big_thumbs": [],
      "bit_rate": [
        {
          "HDR_bit": "",
          "HDR_type": "",
          "bit_rate": 720348,
          "dub_infos": null,
          "gear_name": "adapt_540_1",
          "is_bytevc1": 1,
          "play_addr": {
            "data_size": 4919529,
            "file_cs": "c:0-46577-c445",
            "file_hash": "9728438cd1b5d434a4f2406088dfcb11",
            "height": 1024,
            "uri": "v10025g50000ch9ik0jc77ub16qqnnjg",
            "url_key": "v10025g50000ch9ik0jc77ub16qqnnjg_bytevc1_540p_720348",
            "url_list": [
              "https://v19.tiktokcdn-us.com/422f47cb49d0e1ec92bc607815c11cfb/645642c1/video/tos/alisg/tos-alisg-pve-0037/oQRhWKrsICLBo5KA3TBzNAnKUBAfQsZwEpxyEb/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=1406&bt=703&cs=2&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=11&rc=O2k5PGc2NWk7O2g0Zzc7M0BpanF0OWU6ZjNsazMzODgzNEBeLmIyLTQ2NmAxMy40Xl40YSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
              "https://v16m.tiktokcdn-us.com/ea4a3ce313ed5bc55ba0850bad2aa0af/645642c1/video/tos/alisg/tos-alisg-pve-0037/oQRhWKrsICLBo5KA3TBzNAnKUBAfQsZwEpxyEb/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=1406&bt=703&cs=2&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=11&rc=O2k5PGc2NWk7O2g0Zzc7M0BpanF0OWU6ZjNsazMzODgzNEBeLmIyLTQ2NmAxMy40Xl40YSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
              "https://api16-normal-useast5.us.tiktokv.com/aweme/v1/play/?video_id=v10025g50000ch9ik0jc77ub16qqnnjg&line=0&is_play_url=1&source=PackSourceEnum_CHALLENGE_AWEME&file_id=70a8a47d116e48c89f92730d59e61fa8"
            ],
            "width": 576
          },
          "quality_type": 28
        },
        {
          "HDR_bit": "",
          "HDR_type": "",
          "bit_rate": 433533,
          "dub_infos": null,
          "gear_name": "lower_540_1",
          "is_bytevc1": 1,
          "play_addr": {
            "data_size": 2960761,
            "file_cs": "c:0-46577-3aaa",
            "file_hash": "43bb5f5414642afe67a889a0676d4f40",
            "height": 1024,
            "uri": "v10025g50000ch9ik0jc77ub16qqnnjg",
            "url_key": "v10025g50000ch9ik0jc77ub16qqnnjg_bytevc1_540p_433533",
            "url_list": [
              "https://v19.tiktokcdn-us.com/41d17fc3ea00730d9fc0bc04843557fa/645642c1/video/tos/alisg/tos-alisg-pve-0037/oUaBohneeFvCUVmgpVbOABXCEWtQIQgbgky2XD/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=846&bt=423&cs=2&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=4&rc=O2hnOzlpOjNnZ2dnODZpaUBpanF0OWU6ZjNsazMzODgzNEBhMzQ0LTJhXjUxLjZiNS4xYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
              "https://v16m.tiktokcdn-us.com/f9b6970b26af4979e5554971270e3a8a/645642c1/video/tos/alisg/tos-alisg-pve-0037/oUaBohneeFvCUVmgpVbOABXCEWtQIQgbgky2XD/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=846&bt=423&cs=2&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=4&rc=O2hnOzlpOjNnZ2dnODZpaUBpanF0OWU6ZjNsazMzODgzNEBhMzQ0LTJhXjUxLjZiNS4xYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
              "https://api16-normal-useast5.us.tiktokv.com/aweme/v1/play/?video_id=v10025g50000ch9ik0jc77ub16qqnnjg&line=0&is_play_url=1&source=PackSourceEnum_CHALLENGE_AWEME&file_id=4f1f83e59d1d4d8da0d75f06787d6ed8"
            ],
            "width": 576
          },
          "quality_type": 24
        },
        {
          "HDR_bit": "",
          "HDR_type": "",
          "bit_rate": 326575,
          "dub_infos": null,
          "gear_name": "lowest_540_1",
          "is_bytevc1": 1,
          "play_addr": {
            "data_size": 2230308,
            "file_cs": "c:0-46577-dc2c",
            "file_hash": "92afe33b36efdff5e79191a20bc47b58",
            "height": 1024,
            "uri": "v10025g50000ch9ik0jc77ub16qqnnjg",
            "url_key": "v10025g50000ch9ik0jc77ub16qqnnjg_bytevc1_540p_326575",
            "url_list": [
              "https://v19.tiktokcdn-us.com/b686f9936cb312033f0f3981868a71d6/645642c1/video/tos/alisg/tos-alisg-pve-0037/o0WTB3wKNAIYxUJNQzKybwAnKhAofBIrCZCEEL/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=636&bt=318&cs=2&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=5&rc=NWhlZDY6M2Y2ZTVnOmc0ZkBpanF0OWU6ZjNsazMzODgzNEAzYi9iXl8vNi0xNC82MTQxYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
              "https://v16m.tiktokcdn-us.com/ec78270a56e33141e23bc7071b410ab9/645642c1/video/tos/alisg/tos-alisg-pve-0037/o0WTB3wKNAIYxUJNQzKybwAnKhAofBIrCZCEEL/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=636&bt=318&cs=2&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=5&rc=NWhlZDY6M2Y2ZTVnOmc0ZkBpanF0OWU6ZjNsazMzODgzNEAzYi9iXl8vNi0xNC82MTQxYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
              "https://api16-normal-useast5.us.tiktokv.com/aweme/v1/play/?video_id=v10025g50000ch9ik0jc77ub16qqnnjg&line=0&is_play_url=1&source=PackSourceEnum_CHALLENGE_AWEME&file_id=4c714d972d724b039c20b7a3ea2bee62"
            ],
            "width": 576
          },
          "quality_type": 25
        }
      ],
      "cdn_url_expired": 0,
      "cla_info": {
        "caption_infos": [
          {
            "caption_format": "webvtt",
            "cla_subtitle_id": 7229169230560692994,
            "complaint_id": 7229169230560692994,
            "expire": 1683374785,
            "is_auto_generated": true,
            "is_original_caption": true,
            "lang": "vie-VN",
            "language_code": "vi",
            "language_id": 10,
            "sub_id": -1289841497,
            "sub_version": "1",
            "translator_id": 0,
            "url": "https://v19.tiktokcdn-us.com/01f200890f3cb8c887707356082a3871/645642c1/video/tos/alisg/tos-alisg-pv-0037/4f2d9320a67e422e91c906d5337bf903/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=16336&bt=8168&cs=0&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=13&rc=anF0OWU6ZjNsazMzODgzNEBpanF0OWU6ZjNsazMzODgzNEBna24ucjRnaDZgLS1kLy1zYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9"
          }
        ],
        "captions_type": 1,
        "creator_edited_caption_id": 0,
        "enable_auto_caption": 0,
        "has_original_audio": 0,
        "hide_original_caption": false,
        "original_language_info": {
          "can_translate_realtime": true,
          "is_burnin_caption": false,
          "lang": "vie-VN",
          "language_code": "vi",
          "language_id": 10,
          "original_caption_type": 1
        },
        "vertical_positions": null
      },
      "cover": {
        "height": 720,
        "uri": "tos-alisg-p-0037/e9f6d5a15ef4490d95a3c0229c6be3b1_1683171894",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/e9f6d5a15ef4490d95a3c0229c6be3b1_1683171894?x-expires=1683439200&x-signature=apgWeewzC2eGSiqMHuoKkU1WBLY%3D&s=CHALLENGE_AWEME&se=false&sh=&sc=cover&l=20230506060531760EDB96FF74C50AB8A9"
        ],
        "width": 720
      },
      "cover_is_custom": true,
      "download_addr": {
        "data_size": 9472112,
        "height": 720,
        "uri": "v10025g50000ch9ik0jc77ub16qqnnjg",
        "url_list": [
          "https://v19.tiktokcdn-us.com/9f47f3002207837dc9085f8832348578/645642c1/video/tos/alisg/tos-alisg-pve-0037/ogbKkQJnyJAYv3WTALfhwUzBBKAKyACEICNroZ/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=2708&bt=1354&cs=0&ds=3&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=0&rc=PGc3ZjQ2M2dlNjg8aWg0ZkBpanF0OWU6ZjNsazMzODgzNEBfMGIyLjIyNjIxMmMtNWAxYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
          "https://v16m.tiktokcdn-us.com/71ed404409cee1d7fbe4e8e4598a4465/645642c1/video/tos/alisg/tos-alisg-pve-0037/ogbKkQJnyJAYv3WTALfhwUzBBKAKyACEICNroZ/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=2708&bt=1354&cs=0&ds=3&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=0&rc=PGc3ZjQ2M2dlNjg8aWg0ZkBpanF0OWU6ZjNsazMzODgzNEBfMGIyLjIyNjIxMmMtNWAxYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
          "https://api16-normal-useast5.us.tiktokv.com/aweme/v1/play/?video_id=v10025g50000ch9ik0jc77ub16qqnnjg&line=0&watermark=1&logo_name=tiktok&source=CHALLENGE_AWEME&file_id=4cc18e0ff955435b9d5053115ce43db9"
        ],
        "width": 720
      },
      "duration": 54635,
      "dynamic_cover": {
        "height": 720,
        "uri": "tos-alisg-p-0037/7470f3cebdb5428894c22558722f2750_1683171896",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/obj/tos-alisg-p-0037/7470f3cebdb5428894c22558722f2750_1683171896?x-expires=1683439200&x-signature=7CfAUZzdG7lTZBB9jXgK2SnoCGo%3D&s=CHALLENGE_AWEME&se=false&sh=&sc=dynamic_cover&l=20230506060531760EDB96FF74C50AB8A9"
        ],
        "width": 720
      },
      "has_watermark": true,
      "height": 1024,
      "is_bytevc1": 0,
      "is_callback": true,
      "meta": "{\"LoudnessRange\":\"8.9\",\"LoudnessRangeEnd\":\"-9\",\"LoudnessRangeStart\":\"-17.9\",\"MaximumMomentaryLoudness\":\"-4.2\",\"MaximumShortTermLoudness\":\"-8.3\",\"Version\":\"1\",\"loudness\":\"-12.4\",\"peak\":\"0.75858\",\"qprf\":\"1.000\",\"sr_score\":\"1.000\"}",
      "misc_download_addrs": "{\"suffix_scene\":{\"uri\":\"v10025g50000ch9ik0jc77ub16qqnnjg\",\"url_list\":[\"https://v19.tiktokcdn-us.com/84b6a5e4bc24314d0b30553f8937ac19/645642c1/video/tos/alisg/tos-alisg-pve-0037/osUKzNLBBhcoEFs3CQywfAbTIiKZA9rntAJIWr/?a=1233\&ch=0\&cr=3\&dr=0\&lr=all\&cd=0%7C0%7C0%7C3\&cv=1\&br=2504\&bt=1252\&cs=0\&ds=3\&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~\&mime_type=video_mp4\&qs=0\&rc=OTpnZWRnOWhpaTw0ZjM3ZUBpanF0OWU6ZjNsazMzODgzNEAwMWFgNmNjNS0xMGBhNC42YSNna24ucjRnaDZgLS1kLy1zcw%3D%3D\&l=20230506060531760EDB96FF74C50AB8A9\",\"https://v16m.tiktokcdn-us.com/239021f6857d0872c277054b9083839a/645642c1/video/tos/alisg/tos-alisg-pve-0037/osUKzNLBBhcoEFs3CQywfAbTIiKZA9rntAJIWr/?a=1233\&ch=0\&cr=3\&dr=0\&lr=all\&cd=0%7C0%7C0%7C3\&cv=1\&br=2504\&bt=1252\&cs=0\&ds=3\&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~\&mime_type=video_mp4\&qs=0\&rc=OTpnZWRnOWhpaTw0ZjM3ZUBpanF0OWU6ZjNsazMzODgzNEAwMWFgNmNjNS0xMGBhNC42YSNna24ucjRnaDZgLS1kLy1zcw%3D%3D\&l=20230506060531760EDB96FF74C50AB8A9\",\"https://api16-normal-useast5.us.tiktokv.com/aweme/v1/play/?video_id=v10025g50000ch9ik0jc77ub16qqnnjg\&line=0\&watermark=1\&logo_name=tiktok_end_sonic\&source=CHALLENGE_AWEME\&file_id=9b1470dcc1394f0f8ef6fd9acbdd4736\"],\"width\":720,\"height\":720,\"data_size\":9400177}}",
      "need_set_token": false,
      "origin_cover": {
        "height": 720,
        "uri": "tos-alisg-p-0037/278eaa2b69a14fe5a60023b2d346274f_1683171895",
        "url_list": [
          "https://p16-sign-sg.tiktokcdn.com/tos-alisg-p-0037/278eaa2b69a14fe5a60023b2d346274f_1683171895~tplv-tiktokx-360p.webp?x-expires=1683439200&x-signature=cRSpX0ao1fthh1cvt2jJrDvxn8I%3D&s=CHALLENGE_AWEME&se=false&sh=&sc=feed_cover&l=20230506060531760EDB96FF74C50AB8A9",
          "https://p16-sign-sg.tiktokcdn.com/tos-alisg-p-0037/278eaa2b69a14fe5a60023b2d346274f_1683171895~tplv-tiktokx-360p.jpeg?x-expires=1683439200&x-signature=9zK6VcQmZAYacl83EPR3gqv61HM%3D&s=CHALLENGE_AWEME&se=false&sh=&sc=feed_cover&l=20230506060531760EDB96FF74C50AB8A9"
        ],
        "width": 720
      },
      "play_addr": {
        "data_size": 8551288,
        "file_cs": "c:0-45895-c30a",
        "file_hash": "743e48020c822e45589068c0a4b3418a",
        "height": 1024,
        "uri": "v10025g50000ch9ik0jc77ub16qqnnjg",
        "url_key": "v10025g50000ch9ik0jc77ub16qqnnjg_h264_540p_1252133",
        "url_list": [
          "https://v19.tiktokcdn-us.com/6373f23af037658bc17665c99e337e37/645642c1/video/tos/alisg/tos-alisg-pve-0037/oEZBbKQ5CfrnAAoJWyLBKYwIUhIBNA3zETKj6j/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=2444&bt=1222&cs=0&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=0&rc=OmhnaDloZDU8ZGdpPGU3aEBpanF0OWU6ZjNsazMzODgzNEA2Yy9jMF5fX2ExMmJjXl8vYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
          "https://v16m.tiktokcdn-us.com/b3c988bb1b3ea317427b66a2e94dbee8/645642c1/video/tos/alisg/tos-alisg-pve-0037/oEZBbKQ5CfrnAAoJWyLBKYwIUhIBNA3zETKj6j/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=2444&bt=1222&cs=0&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=0&rc=OmhnaDloZDU8ZGdpPGU3aEBpanF0OWU6ZjNsazMzODgzNEA2Yy9jMF5fX2ExMmJjXl8vYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
          "https://api16-normal-useast5.us.tiktokv.com/aweme/v1/play/?video_id=v10025g50000ch9ik0jc77ub16qqnnjg&line=0&is_play_url=1&source=PackSourceEnum_CHALLENGE_AWEME&file_id=2eb4abf9ef5d4ad9b2baae36fe2dfe97"
        ],
        "width": 576
      },
      "play_addr_bytevc1": {
        "data_size": 4919529,
        "file_cs": "c:0-46577-c445",
        "file_hash": "9728438cd1b5d434a4f2406088dfcb11",
        "height": 1024,
        "uri": "v10025g50000ch9ik0jc77ub16qqnnjg",
        "url_key": "v10025g50000ch9ik0jc77ub16qqnnjg_bytevc1_540p_720348",
        "url_list": [
          "https://v19.tiktokcdn-us.com/422f47cb49d0e1ec92bc607815c11cfb/645642c1/video/tos/alisg/tos-alisg-pve-0037/oQRhWKrsICLBo5KA3TBzNAnKUBAfQsZwEpxyEb/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=1406&bt=703&cs=2&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=11&rc=O2k5PGc2NWk7O2g0Zzc7M0BpanF0OWU6ZjNsazMzODgzNEBeLmIyLTQ2NmAxMy40Xl40YSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
          "https://v16m.tiktokcdn-us.com/ea4a3ce313ed5bc55ba0850bad2aa0af/645642c1/video/tos/alisg/tos-alisg-pve-0037/oQRhWKrsICLBo5KA3TBzNAnKUBAfQsZwEpxyEb/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=1406&bt=703&cs=2&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=11&rc=O2k5PGc2NWk7O2g0Zzc7M0BpanF0OWU6ZjNsazMzODgzNEBeLmIyLTQ2NmAxMy40Xl40YSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
          "https://api16-normal-useast5.us.tiktokv.com/aweme/v1/play/?video_id=v10025g50000ch9ik0jc77ub16qqnnjg&line=0&is_play_url=1&source=PackSourceEnum_CHALLENGE_AWEME&file_id=70a8a47d116e48c89f92730d59e61fa8"
        ],
        "width": 576
      },
      "play_addr_h264": {
        "data_size": 8551288,
        "file_cs": "c:0-45895-c30a",
        "file_hash": "743e48020c822e45589068c0a4b3418a",
        "height": 1024,
        "uri": "v10025g50000ch9ik0jc77ub16qqnnjg",
        "url_key": "v10025g50000ch9ik0jc77ub16qqnnjg_h264_540p_1252133",
        "url_list": [
          "https://v19.tiktokcdn-us.com/6373f23af037658bc17665c99e337e37/645642c1/video/tos/alisg/tos-alisg-pve-0037/oEZBbKQ5CfrnAAoJWyLBKYwIUhIBNA3zETKj6j/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=2444&bt=1222&cs=0&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=0&rc=OmhnaDloZDU8ZGdpPGU3aEBpanF0OWU6ZjNsazMzODgzNEA2Yy9jMF5fX2ExMmJjXl8vYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
          "https://v16m.tiktokcdn-us.com/b3c988bb1b3ea317427b66a2e94dbee8/645642c1/video/tos/alisg/tos-alisg-pve-0037/oEZBbKQ5CfrnAAoJWyLBKYwIUhIBNA3zETKj6j/?a=1233&ch=0&cr=3&dr=0&lr=all&cd=0%7C0%7C0%7C3&cv=1&br=2444&bt=1222&cs=0&ds=6&ft=kLx3-yygZGf0PD1.cYyXg9wa5FdavEeC~&mime_type=video_mp4&qs=0&rc=OmhnaDloZDU8ZGdpPGU3aEBpanF0OWU6ZjNsazMzODgzNEA2Yy9jMF5fX2ExMmJjXl8vYSNna24ucjRnaDZgLS1kLy1zcw%3D%3D&l=20230506060531760EDB96FF74C50AB8A9",
          "https://api16-normal-useast5.us.tiktokv.com/aweme/v1/play/?video_id=v10025g50000ch9ik0jc77ub16qqnnjg&line=0&is_play_url=1&source=PackSourceEnum_CHALLENGE_AWEME&file_id=2eb4abf9ef5d4ad9b2baae36fe2dfe97"
        ],
        "width": 576
      },
      "ratio": "540p",
      "source_HDR_type": 0,
      "tags": null,
      "width": 576
    },
    "video_control": {
      "allow_download": true,
      "allow_duet": true,
      "allow_dynamic_wallpaper": true,
      "allow_music": true,
      "allow_react": true,
      "allow_stitch": true,
      "draft_progress_bar": 1,
      "prevent_download_type": 0,
      "share_type": 1,
      "show_progress_bar": 1,
      "timer_status": 1
    },
    "video_labels": [],
    "video_text": [],
    "voice_filter_ids": null,
    "with_promotional_music": false,
    "without_watermark": false
  }
]
```

### Comment Item Detail

```
[
  {
    "author_pin": false,
    "aweme_id": "7211250685902359850",
    "cid": "7217494551149101851",
    "collect_stat": 0,
    "comment_language": "en",
    "create_time": 1680453949,
    "digg_count": 23,
    "is_author_digged": false,
    "label_list": null,
    "no_show": false,
    "reply_comment": null,
    "reply_comment_total": 5,
    "reply_id": "0",
    "reply_to_reply_id": "0",
    "share_info": {
      "acl": {
        "code": 0,
        "extra": "{}"
      },
      "desc": "🇵🇱 Kasia 🇮🇸's comment: Look it for @Marika Christman . She is doing the best outfits for you. Check it out.",
      "title": "The rehearsal no one saw. Love you all, thanks for being so supportive of a song that means so much to me ❤️",
      "url": "https://www.tiktok.com/@ladygaga/video/7211250685902359850?_d=e80jjb2j1hfl54&_r=1&comment_author_id=7046867863550247941&preview_pb=0&share_comment_id=7217494551149101851&share_item_id=7211250685902359850&sharer_language=en&source=h5_m&u_code=0"
    },
    "status": 1,
    "stick_position": 0,
    "text": "Look it for @Marika Christman . She is doing the best outfits for you. Check it out.",
    "text_extra": [
      {
        "end": 29,
        "hashtag_id": "",
        "hashtag_name": "",
        "sec_uid": "MS4wLjABAAAArXhs1fvcchkAbFNXpJZcD4BSJv7EmPFYcLpK2llb0Fq-K5BFkijKYQlDnHoKL1F6",
        "start": 12,
        "user_id": "7038949358691910662"
      }
    ],
    "trans_btn_style": 0,
    "user": {
      "accept_private_policy": false,
      "account_labels": null,
      "account_region": "",
      "ad_cover_url": null,
      "advance_feature_item_order": null,
      "advanced_feature_info": null,
      "apple_account": 0,
      "authority_status": 0,
      "avatar_168x168": {
        "height": 720,
        "uri": "168x168/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7",
        "url_list": [
          "https://p16-amd-va.tiktokcdn.com/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~tplv-tiktok-shrink:64:64.webp?s=COMMENT_LIST&se=false&sh=64_64&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_168x168.webp?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_168x168.jpeg?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18"
        ],
        "width": 720
      },
      "avatar_300x300": {
        "height": 720,
        "uri": "300x300/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7",
        "url_list": [
          "https://p16-amd-va.tiktokcdn.com/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~tplv-tiktok-shrink:64:64.webp?s=COMMENT_LIST&se=false&sh=64_64&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_300x300.webp?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_300x300.jpeg?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18"
        ],
        "width": 720
      },
      "avatar_larger": {
        "height": 720,
        "uri": "1080x1080/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7",
        "url_list": [
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_1080x1080.webp?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_1080x1080.jpeg?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18"
        ],
        "width": 720
      },
      "avatar_medium": {
        "height": 720,
        "uri": "720x720/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7",
        "url_list": [
          "https://p16-amd-va.tiktokcdn.com/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~tplv-tiktok-shrink:64:64.webp?s=COMMENT_LIST&se=false&sh=64_64&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_720x720.webp?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_720x720.jpeg?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18"
        ],
        "width": 720
      },
      "avatar_thumb": {
        "height": 720,
        "uri": "100x100/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7",
        "url_list": [
          "https://p16-amd-va.tiktokcdn.com/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~tplv-tiktok-shrink:64:64.webp?s=COMMENT_LIST&se=false&sh=64_64&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_100x100.webp?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18",
          "https://p16-amd-va.tiktokcdn.com/img/tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7~c5_100x100.jpeg?s=COMMENT_LIST&se=false&sh=&sc=avatar&l=20230514065113FFB5EBB0D8A8D784DD18"
        ],
        "width": 720
      },
      "avatar_uri": "tos-maliva-avt-0068/7818f08ae60f5417edede76314c0baa7",
      "aweme_count": 0,
      "bind_phone": "",
      "bold_fields": null,
      "can_message_follow_status_list": null,
      "can_set_geofencing": null,
      "cha_list": null,
      "comment_filter_status": 0,
      "comment_setting": 0,
      "commerce_user_level": 0,
      "cover_url": [
        {
          "height": 720,
          "uri": "musically-maliva-obj/1612555907887110",
          "url_list": [
            "https://p16-amd-va.tiktokcdn.com/obj/musically-maliva-obj/1612555907887110"
          ],
          "width": 720
        }
      ],
      "create_time": 0,
      "custom_verify": "",
      "cv_level": "",
      "download_prompt_ts": 1641158568,
      "download_setting": 0,
      "duet_setting": 0,
      "enterprise_verify_reason": "",
      "events": null,
      "favoriting_count": 0,
      "fb_expire_time": 0,
      "follow_status": 0,
      "follower_count": 0,
      "follower_status": 0,
      "followers_detail": null,
      "following_count": 0,
      "friends_status": 0,
      "geofencing": null,
      "google_account": "",
      "has_email": false,
      "has_facebook_token": false,
      "has_insights": false,
      "has_orders": false,
      "has_twitter_token": false,
      "has_youtube_token": false,
      "hide_search": false,
      "homepage_bottom_toast": null,
      "ins_id": "katarzyna.krupinska82",
      "is_ad_fake": false,
      "is_block": false,
      "is_discipline_member": false,
      "is_phone_binded": false,
      "is_star": false,
      "item_list": null,
      "language": "pl",
      "live_agreement": 0,
      "live_commerce": false,
      "live_verify": 0,
      "matched_friend_available": false,
      "mention_status": 1,
      "mutual_relation_avatars": null,
      "need_points": null,
      "need_recommend": 0,
      "nickname": "🇵🇱 Kasia 🇮🇸",
      "platform_sync_info": null,
      "prevent_download": false,
      "react_setting": 0,
      "region": "IS",
      "relative_users": null,
      "room_id": 0,
      "search_highlight": null,
      "sec_uid": "MS4wLjABAAAAZl-oKhIJ9Odmr5H0Nw0rAxgPJgZ16uWIm5pZYxxiJiWcDpPmzOTOu4NbYkgzj9p7",
      "secret": 0,
      "shield_comment_notice": 0,
      "shield_digg_notice": 0,
      "shield_edit_field_info": null,
      "shield_follow_notice": 0,
      "short_id": "0",
      "show_image_bubble": false,
      "signature": "🇵🇱\n🇮🇸",
      "special_account": {
        "special_account_list": null
      },
      "special_lock": 1,
      "status": 1,
      "stitch_setting": 0,
      "total_favorited": 0,
      "tw_expire_time": 0,
      "twitter_id": "",
      "twitter_name": "",
      "type_label": null,
      "uid": "7046867863550247941",
      "unique_id": "katie.kru",
      "unique_id_modify_time": 1684047073,
      "user_canceled": false,
      "user_mode": 1,
      "user_period": 0,
      "user_profile_guide": null,
      "user_rate": 1,
      "user_tags": null,
      "verification_type": 0,
      "verify_info": "",
      "video_icon": {
        "height": 720,
        "uri": "",
        "url_list": [],
        "width": 720
      },
      "white_cover_url": null,
      "with_commerce_entry": false,
      "with_shop_entry": false,
      "youtube_channel_id": "",
      "youtube_channel_title": "",
      "youtube_expire_time": 0
    },
    "user_buried": false,
    "user_digged": 0
  }
]
```

## Limitations

- The scraper retrieves public data only; it does not provide access to private data.
- Pagination support is not available at the moment, but it can be requested as a feature.
- TikTok's usage policies and limitations apply when using the scraper.
- Consideration for TikTok's rate limiting and throttling is not provided within the scraper.
- Known limitations or issues are primarily related to TikTok's limitations.

## Ethical Use and Data Practices

Our TikTok Scraper operates **without logging in to TikTok**. This means it **doesn't implicitly accept any of TikTok's
Terms of Service (ToS) that require a login**, as we only process data that's **publicly displayed and accessible to
everyone** without authentication.

We're fully committed to the principle of **privacy by design and by default**. All data collected **explicitly excludes
sensitive personal information or non-public data**.

Furthermore, our scraper runs on **Apify, an EU-based company**, which means our operations are designed to be *
*compliant with relevant EU data protection regulations**, including GDPR, where applicable. You can find more
information about the legality of web scraping on Apify's
blog: [https://blog.apify.com/is-web-scraping-legal/](https://blog.apify.com/is-web-scraping-legal/)

We've implemented robust technical measures to ensure the scraper
operates gently and **doesn't impose an undue burden on TikTok's servers**. Our sole purpose is to facilitate *
*responsible research and public data analysis**, and we strictly prohibit any use that could cause harm to any party or
the platform itself.

## Customization and Extension

The Fast TikTok API Scraper can be customized or extended based on your specific requirements. You can make a ticket on
the Apify actor to request additional functionalities or customization.

**Our customers have ordered these customized actors:**

| Scraper | Link |
| --- | --- |
| **Fast TikTok with Simple Result** | [Fast TikTok with Simple Result](https://apify.com/novi/fast-tiktok-api-with-simple-result?fpr=7hce1m) |
| **TikTok AI Video Scraper** | [TikTok AI Video Scraper](https://apify.com/novi/tiktok-ai-video-scraper?fpr=7hce1m) |
| **TikTok Music Trend API** | [Tiktok Music Trend API](https://apify.com/novi/tiktok-music-trend-api?fpr=7hce1m) |
| **Tiktok Multiple Hashtag Scraper** | [Tiktok Multiple Hashtag Scraper](https://apify.com/novi/multiple-tiktok-hashtag-scraper?fpr=7hce1m) |
| **Tiktok Scraper Ultimate (pay-per-event)** | [Tiktok Scraper Ultimate (pay-per-event)](https://apify.com/novi/tiktok-scraper-ultimate?fpr=7hce1m) |

## Cost

The scraper offers a 1-day trial period, and after that, it requires a subscription of $35 per month.

## Scrape any TikTok data you need with dedicated scrapers

If you want to get specific data from TikTok, you can use the scrapers below. Each scraper is made to help you get
different kinds of TikTok data, like hashtags, search results, profiles, or everything at once. You can look at them to
see which one you need.

| Scraper | Link |
| --- | --- |
| 👥 TikTok Followers API | [TikTok Followers API](https://apify.com/novi/tiktok-followers-api?fpr=7hce1m) |
| 🎙 TikTok Comment API | [TikTok Comment API](https://apify.com/novi/tiktok-comment-api?fpr=7hce1m) |
| 📹 TikTok Trend API | [TikTok Trend API](https://apify.com/novi/tiktok-trend-api?fpr=7hce1m) |
| 🔍 TikTok Search API | [TikTok Search API](https://apify.com/novi/tiktok-search-api?fpr=7hce1m) |
| 🧛 TikTok User API | [TikTok User API](https://apify.com/novi/tiktok-user-api?fpr=7hce1m) |
| 🎸 TikTok Music API | [TikTok Music API](https://apify.com/novi/tiktok-sound-api?fpr=7hce1m) |
| 🧛 TikTok User Info API | [TikTok User Info API](https://apify.com/novi/tiktok-user-info-api?fpr=7hce1m) |
| #️⃣ TikTok Hashtag API | [TikTok Hashtag API](https://apify.com/novi/tiktok-hashtag-api?fpr=7hce1m) |
| 🛍 TikTok Shop API | [TikTok Shop API](https://apify.com/novi/tiktok-shop-scraper?fpr=7hce1m) |
| 🛍 Tiktok Scraper Ultimate (pay-per-event) | [Tiktok Scraper Ultimate (pay-per-event)](https://apify.com/novi/tiktok-scraper-ultimate?fpr=7hce1m) |
| 🐦 Twitter - X.com Scraper | [🐦 Twitter - X.com Scraper](https://apify.com/xtdata/twitter-x-scraper?fpr=7hce1m) |