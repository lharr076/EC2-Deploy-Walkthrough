<h1><p align="center">EC2 Deploy Walkthrough<p align="center"></p></h1>
<p align="center">
  <h2><p align="center">Step 1<p align="center"></p></h2>
  <p align="center">
    <a href="https://imgur.com/shcBlVf"><img src="https://i.imgur.com/shcBlVf.png" title="source: imgur.com" /></a>
    <br />
    <br />
    <a href="https://imgur.com/B4kJGjv"><img src="https://i.imgur.com/B4kJGjv.png?1" title="source: imgur.com" /></a>
    <br />
    This is a new set of access keys I needed to generate for my user. I choose to do this for two reasons, 1. I needed to for security reasons and to show simple it is. I logged into my AWS account and in the search bar I search IAM and at the IAM dashboard I select    my name, create access key. To make your life easier, give your key a tag. I collected my keys then jetted over to the CLI.
    <p align="center">
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 2<p align="center"></p></h2>
  <p align="center">
    <a href="https://imgur.com/bdSY4QZ"><img src="https://i.imgur.com/bdSY4QZ.png" title="source: imgur.com" /></a>
  <br />
  The local user needed to have AWS CLI installed so I installed it by simply downloading it from here https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html and next configuring my IAM creds in prep for Terraform.(Not displayed) As I navigated      through AWS configure, I did have to input my default region which in my case is US-EAST-1.
   <p align=""center> 
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 3<p align="center"></p></h2>
  <p align="center">   
  <a href="https://imgur.com/GUo2WHF"><img src="https://i.imgur.com/GUo2WHF.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/BUCJOtT"><img src="https://i.imgur.com/BUCJOtT.png" title="source: imgur.com" /></a>
  After I set my configurations, I create a directory called <i>terraform-aws-instance</i> to house my infrastructure file/s. The directory is made and <i>cd terraform-aws-instance</i> command changes me into that directory to prepare for creating the file to house my code.
  <p align="center">  
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 4<p align="center"></p></h2>
  <p align="center">
    <p align="center"><a href="https://imgur.com/vpV2F3T"><img src="https://i.imgur.com/vpV2F3T.png" title="source: imgur.com" /></a><p align="center">
  I have VS Code installed so I simply typed <i>code Main.tf</i> to open the app and I input my information before saving the file in my respective folder. A note I would recommend, if you are referencing someone elses code, review it, take the due diligence to look up the ami id to confirm it is still availabile and so forth. This is something I have ran into in the past my very first time trying out Terraform.
    <p align="center">
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 5<p align="center"></p></h2>
  <p align="center">    
  <a href="https://imgur.com/253BQX3"><img src="https://i.imgur.com/253BQX3.png" title="source: imgur.com" /></a>
  <br /> 
  I navigated back over to the command prompt, I made sure I was still in my terraform folder and proceeded with the command <i>terraform init</i> and success the config has been initialized. Initializing with Terraform downloads and installs the providers configured in the code, which in this case is AWS.
   <p align="center"> 
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 6<p align="center"></p></h2>
  <p align="center">   
  <a href="https://imgur.com/wzzxcFu"><img src="https://i.imgur.com/wzzxcFu.png" title="source: imgur.com" /></a>
  <br />  
  I like to try and create good habits with things I am new to and that is what <i>terraform fmt</i> does. This will help give your configuration readability and consistency and this command will print out anything that may have been modified. This is really a cool tool because this can help rule out mistakes because we are all human.
  <p align="center">  
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 7<p align="center"></p></h2>
  <p align="center"> 
  <a href="https://imgur.com/HpmriNq"><img src="https://i.imgur.com/HpmriNq.png" title="source: imgur.com" /></a>
  <br /> 
  I input <i>terraform validate</i> to make sure my configuration is syntactically valid and internally consistent. How I interpret this is more checks and balances to the <i>fmt</i> command.
  <p align="center">   
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 8<p align="center"></p></h2>
  <p align="center">  
  <a href="https://imgur.com/J6rdsH7"><img src="https://i.imgur.com/J6rdsH7.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/WarNJwP"><img src="https://i.imgur.com/WarNJwP.png" title="source: imgur.com" /></a>
  <br  />
  <br />
  <a href="https://imgur.com/91XbRUZ"><img src="https://i.imgur.com/91XbRUZ.png" title="source: imgur.com" /></a>
  After typing <i>yes</i> to apply the terraform config, I have my first issue which is no default vpc for this user. So I navigate back to VS Code and add my cloudLab-vpc subnet that I use for my projects. I save the modified code and attempted my deploy again.
  <p align="center">
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 9<p align="center"></p></h2>
  <p align="center">  
  <a href="https://imgur.com/0nokbhG"><img src="https://i.imgur.com/0nokbhG.png" title="source: imgur.com" /></a>
  I navigate back to AWS EC2 dashboard to confirm my code deployed.
  <p align="center">  
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 10<p align="center"></p></h2>
  <p align="center">  
  <a href="https://imgur.com/57bCapo"><img src="https://i.imgur.com/57bCapo.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/YToUrxB"><img src="https://i.imgur.com/YToUrxB.png" title="source: imgur.com" /></a>
  Something to check out that I thought was neat and bears more useful information is <i>terraform show</i>. With terraform show, you can inspect the current state displaying the resource ami-id, subnet-id and other useful information.
  <p align="center">  
  <br />
  <br />
  <br />
  <br />
  <h2><p align="center">Step 11<p align="center"></p></h2>
  <p align="center">  
  <a href="https://imgur.com/DT9UAnA"><img src="https://i.imgur.com/DT9UAnA.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/LoBAcQw"><img src="https://i.imgur.com/LoBAcQw.png" title="source: imgur.com" /></a>
  <br />
  <br />
  <a href="https://imgur.com/LO1DghD"><img src="https://i.imgur.com/LO1DghD.png" title="source: imgur.com" /></a>
  After checking out the state, I went ahead and did a tear down of the infrastructure with the <i>terraform destroy</i> command. After the command, I nav back over to the EC2 dashboard to confirm.
    <p align="center">
  <br />    
  <h2><p align="center">Afterthoughts<p align="center"></p></h2>
    <p align="center">
      The purpose behind myself tackling this is to work on even fundemental skills such as deleting and creating a new public and secret AWS keys, spending time in the CLI and working from there as much as possible to build strength, untilizing VS Code and having some minor troubleshooting in some areas that I will address next. As a mechanic and early IT troubleshooting, even the simple tasks can have issues that may throw you for a loop. As I grow to understand technical mechanics of tech, I am able to see the overlap ensuring with time I will be very good at what will be needed. Minor issues that were resolved before the VPC issue were, deleting old AWS access keys for my IAM role since the keys were over 100 days old, creating a new local user on my desktop, installing AWS CLI on the local user, I already had Terraform on path so I did not need to install, I had to setup AWS configure on the new local account with the new AWS access keys, and update my VS Code software to aid in setting the stage for deployment. Running into not having a default VPC, I step back I read it to comprehend. Even if one may be seasoned, there is no shame in having a cheat sheet or reference guides to aid in your tasks. Assessing the issue, I read through Terraform documentation, referenced Stack Overflow, to help me confirm what I suspected. I navigate to my AWS VPC dashboard to collect a public subnet-id to use within my main.tf file within the resource of the instance. After running the processes again, the infrastructure is built with the one example instance in the cloud, I run the terraform state command in the CLI to inspect the state of what has been executed. After destroying the infrastructure I confirm in the AWS dashboard to aid in keeping cost down. 
    <p align="center">  
<p align="center">
