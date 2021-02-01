# tags -- git tags
{:data-section="git"}
{:data-date="December 03, 2019"}
{:data-extra="Um Pages"}

## SYNOPSIS

Git Tags `https://git-scm.com/book/en/v2/Git-Basics-Tagging`

## COMMANDS

`git tag -a v1.4 -m "my version 1.4"`
: *Annotated tags* are stored as full objects in the Git database. They’re checksummed; contain the tagger name, email, and date; have a tagging message; and can be signed and verified with GNU Privacy Guard (GPG). It’s generally recommended that you create annotated tags so you can have all this information; but if you want a temporary tag or for some reason don’t want to keep the other information, lightweight tags are available too.

`git tag v1.4-lw`
: A *lightweight tag* is basically the commit checksum stored in a file — no other information is kept. To create a lightweight tag, don’t supply any of the -a, -s, or -m options, just provide a tag name.

`git show v1.4`
: You can see the tag data along with the commit that was tagged

`git tag`
: List all tags


By default, the git push command doesn't transfer tags to remote servers. You will have to explicitly push tags to a shared server after you have created them. This process is just like sharing remote branches — you can run git push \<origin\> \<tagname\>.

`git push origin v1.4`
: Push a specific tag to \<origin\>

`git push origin --tags`
: Transfer all of your tags to the remote server that are not already there.

`git tag -d v1.4-lw`
: Delete a tag on your local repository. Note that this does not remove the tag from any remote servers.

`git push origin --delete v1.4-`
: Delete a tag on remote \<origin\>
