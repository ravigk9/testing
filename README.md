# testing
http://scriptedonachip.com/git-sparse-checkout
$ mkdir pcl-examples
$ cd pcl-examples								#make a directory we want to copy folders to
$ git init                            			#initialize the empty local repo
$ git remote add origin -f https://github.com/PointCloudLibrary/pcl.git     #add the remote origin
$ git config core.sparsecheckout true			#very crucial. this is where we tell git we are checking out specifics
$ echo "examples/*" >> .git/info/sparse-checkout" #recursively checkout examples folder
$ git pull --depth=2 origin master			#go only 2 depths down the examples directory

https://askubuntu.com/questions/460885/how-to-clone-git-repository-only-some-directories
git init <repo>
cd <repo>
git remote add -f origin <url>

git config core.sparseCheckout true

echo "some/dir/" >> .git/info/sparse-checkout
echo "another/sub/tree" >> .git/info/sparse-checkout

https://coderwall.com/p/mglmxa/checkout-a-single-folder-from-a-github-repository

https://coderwall.com/p/mglmxa/checkout-a-single-folder-from-a-github-repository

mkdir <repo>
cd <repo>
git init
git remote add -f origin <url>
  git config core.sparseCheckout true
  echo "some/dir/" >> .git/info/sparse-checkout
echo "another/sub/tree" >> .git/info/sparse-checkout
  git pull origin master
  
  
  git init
git remote add -f origin <url>
git config core.sparsecheckout true
echo <dir1>/ >> .git/info/sparse-checkout
echo <dir2>/ >> .git/info/sparse-checkout
echo <dir3>/ >> .git/info/sparse-checkout
git pull origin master
  
  https://stackoverflow.com/questions/2425059/how-to-pull-specific-directory-with-git
