# Contact Email Lambda
A simple endpoint to take a JSON body from a form that forwards it as an email using Amazon's Simple Email Service.

## Usage
1. Install serverless to your machine:
  npm install -g serverless

2. [Set up your AWS IAM account](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html)

3. Configure serverless with your credentials:
```
serverless config credentials \
    --provider aws \
    --key xxxxxxxxxxxxxx \
    --secret xxxxxxxxxxxxxx
```

4. Create `secrets.json` in the root folder, follow the example in `secrets.example.json` to fill in the necessary parameters.

5. Ship it!
  serverless deploy

6. Grab the endpoint URL from the console output and hook it up to your form using the POST body below.

### Body
```
{
  "email":"reply@email.com",
  "name":"Contact Name",
  "content":"Message here"
}
```

This repo relies heavily on [this blog post by Adnan Rahic], thanks for the awesome info.