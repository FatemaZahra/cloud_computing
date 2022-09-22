## Store S3 bucket logs

1. Create a new bucket to store the logs of (another/previously created) bucket. Follow [link](https://github.com/FatemaZahra/cloud_computing/blob/main/S3-bucket/S3bucket.md) for steps to create a bucket.

2. Go to the bucket for which the logs are to be stored and Click on **Properties**
<img width="944" alt="Screenshot 2022-09-22 at 15 51 53" src="https://user-images.githubusercontent.com/102330725/191780216-79ddc4f1-1815-4a68-9ad3-c3af4e928b0b.png">

3. Scroll down to **Server access logging** settings and Click on **Edit**
<img width="944" alt="Screenshot 2022-09-22 at 15 52 51" src="https://user-images.githubusercontent.com/102330725/191780442-ee20f444-e063-49d3-a676-1c4359aade76.png">

4. Click on **Enable** and in Target Bucket, add the newly created bucket name in which the logs are to be stored and **Save Changes**
<img width="847" alt="Screenshot 2022-09-22 at 15 54 26" src="https://user-images.githubusercontent.com/102330725/191780846-8b54e248-9220-4fba-a335-610d06d51458.png">

The logs generated are stored in the target bucket.
<img width="956" alt="Screenshot 2022-09-22 at 16 19 41" src="https://user-images.githubusercontent.com/102330725/191786836-50c9e2b5-7ac9-4cd8-85f1-99fb7338a5d7.png">
