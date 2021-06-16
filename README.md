teraform fmt -- formate the .tf file  
terrafrom workspace new workspace  --create workspaces in isolated state 
terrafrom state-- list pull mv workspaces 
terraform taint-- deletes  and recreates the resource
terrform import---- imports already manually created resource 
terraform init-- download the provider modules for provisioning 
terrafrom plan--  shows the resource plans that are going to be orchestrated
terrafrom apply--  creates teh resource 
terrafrom destroy-- deletes the resoure 
terrafrom workspace select newworkspace --  select a different workspace 
TF_LOG=dEBUG terrafrom apply -- run terrafrom in debug mode 
