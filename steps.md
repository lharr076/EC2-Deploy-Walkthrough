<p align="center">
<a href="https://imgur.com/shcBlVf"><img src="https://i.imgur.com/shcBlVf.png" title="source: imgur.com" /></a>
<a href="https://imgur.com/B4kJGjv"><img src="https://i.imgur.com/B4kJGjv.png?1" title="source: imgur.com" /></a>
This is a new set of access keys I needed to generate for my user.
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/bdSY4QZ"><img src="https://i.imgur.com/bdSY4QZ.png" title="source: imgur.com" /></a>
The local user needed to have AWS CLI installed so I installed it by simply downloading it(insert link here) and next configuring my IAM creds in prep for Terraform.
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/GUo2WHF"><img src="https://i.imgur.com/GUo2WHF.png" title="source: imgur.com" /></a>
  <a href="https://imgur.com/BUCJOtT"><img src="https://i.imgur.com/BUCJOtT.png" title="source: imgur.com" /></a>
After I set my parameters, I create a directory to prepare for my infrastructure files. Then change into that directory
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/vpV2F3T"><img src="https://i.imgur.com/vpV2F3T.png" title="source: imgur.com" /></a>
 I have VS Code installed so I simply typed code. Main.tf to open the app and I input my information before saving the file in my respective folder.
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/253BQX3"><img src="https://i.imgur.com/253BQX3.png" title="source: imgur.com" /></a>
I navigated back over to the command prompt, made sure I was still in my terraform folder and proceeded with the command terraform init and success the config has been initialized.
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/wzzxcFu"><img src="https://i.imgur.com/wzzxcFu.png" title="source: imgur.com" /></a>
I like to try and create good habits and that is what terraform fmt does. This will help give your configuration readability and consistency and this command will print out anything that may have been modified.
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/HpmriNq"><img src="https://i.imgur.com/HpmriNq.png" title="source: imgur.com" /></a>
I input terraform validate to make sure my configuration is syntactically valid and internally consistent
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/J6rdsH7"><img src="https://i.imgur.com/J6rdsH7.png" title="source: imgur.com" /></a>
  <a href="https://imgur.com/WarNJwP"><img src="https://i.imgur.com/WarNJwP.png" title="source: imgur.com" /></a>
  <a href="https://imgur.com/91XbRUZ"><img src="https://i.imgur.com/91XbRUZ.png" title="source: imgur.com" /></a>
After typing yes to apply the terraform config, I have my first issue which is no default vpc for this user. So I navigate back to VS Code and add my cloudLab-vpc that I use for my projects. I save and try again
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/0nokbhG"><img src="https://i.imgur.com/0nokbhG.png" title="source: imgur.com" /></a>
I navigate back to AWS EC2 dashboard to confirm my code deployed
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/57bCapo"><img src="https://i.imgur.com/57bCapo.png" title="source: imgur.com" /></a>
  <a href="https://imgur.com/YToUrxB"><img src="https://i.imgur.com/YToUrxB.png" title="source: imgur.com" /></a>
Something to check out that I thought was neat and bears more useful information is terraform show. With terraform show, you can inspect the current state
  <br />
  <br />
  <br />
  <br />
  <a href="https://imgur.com/DT9UAnA"><img src="https://i.imgur.com/DT9UAnA.png" title="source: imgur.com" /></a>
  <a href="https://imgur.com/LoBAcQw"><img src="https://i.imgur.com/LoBAcQw.png" title="source: imgur.com" /></a>
  <a href="https://imgur.com/LO1DghD"><img src="https://i.imgur.com/LO1DghD.png" title="source: imgur.com" /></a>
After checking out the state, I went ahead and did a tear down of the infrastructure with the terraform destroy command. After the command, i nav back over to the EC2 dashboard to confirm.
<p align="center">
