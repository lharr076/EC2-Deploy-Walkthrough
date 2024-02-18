<h1><p align="center">EC2 Deploy Walkthrough<p align="center"></p></h1>
<p align="center">
  <h2><p align="center">Step 1<p align="center"></p></h2>
  <a href="https://imgur.com/shcBlVf"><img src="https://i.imgur.com/shcBlVf.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/B4kJGjv"><img src="https://i.imgur.com/B4kJGjv.png?1" title="source: imgur.com" /></a>
  <br />
  This is a new set of access keys I needed to generate for my user. I choose to do this for two reasons, 1. I needed to for security reasons and to show simple it is. I logged into my AWS account and in the search bar I search IAM and at the IAM dashboard I select my     name create access key. To make your life easier, give your key a tag. I collected my keys then jetted over to the CLI.
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 2<p align="center"></p></h2>
  <a href="https://imgur.com/bdSY4QZ"><img src="https://i.imgur.com/bdSY4QZ.png" title="source: imgur.com" /></a>
  <br />
  The local user needed to have AWS CLI installed so I installed it by simply downloading it from here https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html and next configuring my IAM creds in prep for Terraform.(Not displayed) As I navigated      through the AWS config, I did have to input my default region which in my case is US-EAST-1.
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 3<p align="center"></p></h2>
  <a href="https://imgur.com/GUo2WHF"><img src="https://i.imgur.com/GUo2WHF.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/BUCJOtT"><img src="https://i.imgur.com/BUCJOtT.png" title="source: imgur.com" /></a>
  After I set my config, I create a directory called terraform-aws-instance to house my infrastructure file/s. The directory is made and cd terraform-aws-instance command changes me into that directory to prepare for creating the file to house my code.
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 4<p align="center"></p></h2>
  <p align="center"><a href="https://imgur.com/vpV2F3T"><img src="https://i.imgur.com/vpV2F3T.png" title="source: imgur.com" /></a><p align="center">
  I have VS Code installed so I simply typed code Main.tf to open the app and I input my information before saving the file in my respective folder. A note I would recommend, if you are referencing someone elses code, review it, take the due diligence to look up the       ami id to confirm it is still availabile and so forth. This is something I have ran into in the past my very first time trying out Terraform.
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 5<p align="center"></p></h2>  
  <a href="https://imgur.com/253BQX3"><img src="https://i.imgur.com/253BQX3.png" title="source: imgur.com" /></a>
  <br /> 
  I navigated back over to the command prompt, made sure I was still in my terraform folder and proceeded with the command terraform init and success the config has been initialized. Initializing with Terraform downloads and installs the providers configured in the        code, which in this case is AWS.
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 6<p align="center"></p></h2>  
  <a href="https://imgur.com/wzzxcFu"><img src="https://i.imgur.com/wzzxcFu.png" title="source: imgur.com" /></a>
  <br />  
  I like to try and create good habits with things I am new to and that is what terraform fmt does. This will help give your configuration readability and consistency and this command will print out anything that may have been modified. This is really a cool tool          because this can help rule out mistakes because we are all human.
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 7<p align="center"></p></h2>  
  <a href="https://imgur.com/HpmriNq"><img src="https://i.imgur.com/HpmriNq.png" title="source: imgur.com" /></a>
  <br /> 
  I input terraform validate to make sure my configuration is syntactically valid and internally consistent. How I interpret this is more checks and balances to the fmt command.
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 8<p align="center"></p></h2>  
  <a href="https://imgur.com/J6rdsH7"><img src="https://i.imgur.com/J6rdsH7.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/WarNJwP"><img src="https://i.imgur.com/WarNJwP.png" title="source: imgur.com" /></a>
  <br  />
  <br />
  <a href="https://imgur.com/91XbRUZ"><img src="https://i.imgur.com/91XbRUZ.png" title="source: imgur.com" /></a>
  After typing yes to apply the terraform config, I have my first issue which is no default vpc for this user. So I navigate back to VS Code and add my cloudLab-vpc that I use for my projects. I save and try again
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 9<p align="center"></p></h2>  
  <a href="https://imgur.com/0nokbhG"><img src="https://i.imgur.com/0nokbhG.png" title="source: imgur.com" /></a>
  I navigate back to AWS EC2 dashboard to confirm my code deployed
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 10<p align="center"></p></h2>  
  <a href="https://imgur.com/57bCapo"><img src="https://i.imgur.com/57bCapo.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/YToUrxB"><img src="https://i.imgur.com/YToUrxB.png" title="source: imgur.com" /></a>
  Something to check out that I thought was neat and bears more useful information is terraform show. With terraform show, you can inspect the current state
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 11<p align="center"></p></h2>  
  <a href="https://imgur.com/DT9UAnA"><img src="https://i.imgur.com/DT9UAnA.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/LoBAcQw"><img src="https://i.imgur.com/LoBAcQw.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/LO1DghD"><img src="https://i.imgur.com/LO1DghD.png" title="source: imgur.com" /></a>
  After checking out the state, I went ahead and did a tear down of the infrastructure with the terraform destroy command. After the command, i nav back over to the EC2 dashboard to confirm.
<p align="center">
