# Git Tag

### Git create tag
`git tag <tagname>`

### List/View all Git Tag
`git tag -l "v2.*"`

### Push all Git Tag
`git push origin --tags`

### Push a specific Tag
`git push origin tag_a` or `git push origin refs/tags/tag_a`

### Delete a local tag
`git tag -d <tagname>`

### Delete all local tag
`git tag -d $(git tag -l)`

### Delete all remote tag
`git push origin --delete $(git tag -l)`

### Checkout 
`git checkout tags/version 1.0`
