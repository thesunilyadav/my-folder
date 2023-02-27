# How to clone specific folder in git

git init <repo>
cd <repo>
git remote add -f origin <url>

git config core.sparseCheckout true

echo "some/dir/" >> .git/info/sparse-checkout
echo "another/sub/tree" >> .git/info/sparse-checkout

This tells git which directories you want to checkout. Then you can pull just those directories

git pull origin master
