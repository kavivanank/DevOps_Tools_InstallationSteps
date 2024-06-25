**For linux(ubuntu),** Run the below commands one by one.

``wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg``

``echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list``

``sudo apt update && sudo apt install terraform``

For latest commands, visit the url
https://developer.hashicorp.com/terraform/install#linux

____________________________________________________________________________________________________

**For Windows OS,** install manually from the below url

https://developer.hashicorp.com/terraform/install#windows

1. Extract the zip file and check for the terraform.exe file.

2. Go to Environment Variables > Edit 'Path' in both User Variables and System Variables > Add the path of terraform file followed by \.

3. Save by clicking Ok.

4. Open VS Code and install Hashicorp Terraform extension.

5. Open Command terminal and run the command ``$Env:Path`` to verify environment variables added in step-2.

6. Now verify by executing ``terraform`` or ``terraform --version``.
