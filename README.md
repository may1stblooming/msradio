mkdir gpt-privacy
cd gpt-privacy
echo "<html><body><h1>Privacy Policy</h1><p>This GPT does not store personal data.</p></body></html>" > index.html
git init
git add .
git commit -m "Add policy"
gh repo create yourusername/gpt-privacy --public --source=. --remote=origin
git push -u origin main
gh pages --publish .
