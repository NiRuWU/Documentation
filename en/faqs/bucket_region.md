
---
title: How can I choose the region of my cloud storage?
description: 
platform: All Platforms
updatedAt: Wed Mar 25 2020 22:49:47 GMT+0800 (CST)
---
# How can I choose the region of my cloud storage?
Agora Cloud Recording supports the following cloud storage vendors:

- Qiniu Cloud
- Amazon S3
- Alibaba Cloud
- Tencent Cloud

Before you start, ensure that you have enabled cloud storage service with at least one of the above-mentioned vendors and have created a bucket. When calling `start`, you need to enter your cloud storage information: When setting `storageConfig`, choose a region close to the server from which you send your recording request. See [Agora Cloud Recording RESTful API](../../en/cloud-recording/cloud_recording_api_rest.md) for more information.

## Issues with cross-region upload

The files to upload to the cloud storage are stored on the servers close to where you make the recording request. Therefore, a cross-region upload, e.g., making the request in the U.S. while setting the region to Beijing, can be slow or even fail.

## Solution
Because a cross-region upload takes much more time and is more likely to fail, avoid using this approach when possible.
