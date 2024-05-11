# Private S3 bucket static website using CloudFront 

## `Instruction:`

> Create a static website and host it on S3 bucket(private bucket) but with public read policy assigned, using cloud front for CDN.

## Steps:

## `s3 Bucket setup`

- Firstly, login to your AWS account and search for `s3` in the searchbox

![s3 bucket](/img/search-s3.png)

- Click `s3` and click on `create bucket`

![s3 bucket](/img/create-bucket.png)


- Input a unique name for your bucket and leave everything else as default and click on `create bucket` on the bottom of the screen.

![s3 bucket](img/name-bucket.png)

![s3 bucket](img/block-pub-access.png)

![s3 bucket](img/bucket-named.png)


- On the next page,click on the bucket name then click on the icon `upload` and click add folder to upload your website files

![s3 bucket](img/bucket-created.png)

![s3 bucket](img/upload.png)

![s3 bucket](img/uploaded.png)

- After successfully uploading, click on the folder name to view its content, select all files, then go to `action` dropdown and move all files to the root folder (bucket name).

![s3 bucket](img/move.png)

![s3 bucket](img/moved.png)



## `Next is to ssetup our cloudfront`

- Go to Searchbox and search CloudFront, then click on it.


![cloudfront](img/search-cloudfront.png)

- Click on create new distribution. 


![cloudfront](img/create-cloudfront.png)

- Input domain name. After selecting your bucket name scroll down to `Origin access` and select `Origin access control settings(recommended)` to create a new origin access control OAC and scroll down to enable security. Then click `create distribution`

![origin](img/origin-name.png)

![distribution](img/enable-security.png)

![distribution](img/distribution.png)


- After CloudFront distribution has been created. Click on `Copy Policy`

![policy](img/copy-policy.png)

- Then go back to S3 console and go to s3 bucket permissions tab. Scroll down to bucket policy and click `edit` and paste policy into the textbox

![bucket-policy](img/edit-bucket.png)

![bucket-policy](img/paste-policy.png)

![bucket-policy](img/policy-created.png)


- Then back to the created CloudFront distribution to copy your `distribution domain name`

![domain](img/copy-dns.png)

- Paste on a new tab to view our website.

![website](img/website.png)