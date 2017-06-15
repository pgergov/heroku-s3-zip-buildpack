# Heroku S3 Zip Download Buildpack

This is a Heroku Buildpack that can download (zip) files from a public Amazon S3-bucket. It will create a folder called `s3files` in the root directory of your project and download the files inside it. If any of the file's extension is `.zip` it will unzip it and put the result in the same file.


## Usage
  - In your project root directory create a file and call it `.build` and put inside it all files you want to download from your bucket.

  - **Important** Put one file at each line. If you have only one file remember to add an `empty row` at the end.
  
```
binary1.exe
binary2.tar.gz
binary3.dll
```
  
  - You will need to add the following environment variables:

```
AWS_BUCKET=xxxxxxxxxxxxxxxxxxxxxxx
AWS_REGION=xxxxxxxxxxxxxxxxxxxxxxx
BRANCH_FOLDER=xxxxxxxxxxxxxxxxxxxxxxx
```

  - This buildpack is based on the [official custom buildpack documentation](https://devcenter.heroku.com/articles/buildpack-api)
