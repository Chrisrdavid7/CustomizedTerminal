# CustomizedTerminal

Terminal Design

Type nanop and 
copy and paste the information from below 

Change your text color to grey.

Enjoy!!!

export PS2="| "
#-------------------------------------------------------#

#   Set Paths#
#   ------------------------------------------------------------   #
export PATH="/usr/local/bin/$PATH:"
export PATH="/usr/local/git/bin:/sw/bin/:/usr/local/bin:/usr/local/:/usr/local/sbin:/usr/local/mysql/bin:$PATH"
#--------------------------------------------------------#


#  Git Info  #
# ---------- #
function parse_git_branch {
ref=$(git symbolic-ref HEAD 2> /dev/null) || return
echo "("${ref#refs/heads/}")"
}

function parse_git_branch {
ref=$(git symbolic-ref HEAD 2> /dev/null) || return
echo "("${ref#refs/heads/}")"
}

RED="\[\033[0;31m\]"
YELLOW="\[\033[0;33m\]"
GREEN="\[\033[0;32m\]"

PS1="$RED\$(date +%H:%M) \w$YELLOW \$(parse_git_branch)$GREEN\$ "


# Terminal Colors and Alias #
#___________________________#


export CLICOLOR=1
export LSCOLORS=ExFxCxDxBxegedabagacad
alias ls='ls -GFh'
alias nanop='nano .bash_profile'

#​_--_​--​_--_​--​_--_​--​_--_​#

C_DEFAULT="\[\033[m\]"
WHITE="\[\033[0;97m\] "
GREEN="\[\033[0;92m\]"

# Regular Colors #
# \[\033[0;30m\] # Black  #
# \[\033[0;31m\] # Red    #
# \[\033[0;32m\] # Green  #
# \[\033[0;33m\] # Yellow #
# \[\033[0;34m\] # Blue   #
# \[\033[0;35m\] # Purple #
# \[\033[0;36m\] # Cyan   #
# \[\033[0;37m\] # White  #

# High Intensty #
# \[\033[0;90m\] # Black  #
# \[\033[0;91m\] # Red    #
# \[\033[0;92m\] # Green  #
# \[\033[0;93m\] # Yellow #
# \[\033[0;94m\] # Blue   #
# \[\033[0;95m\] # Purple #
# \[\033[0;96m\] # Cyan   #
# \[\033[0;97m\] # White  #

# Background #
# \[\033[40m\] # Black    #
# \[\033[41m\] # Red      #
# \[\033[42m\] # Green    #
# \[\033[43m\] # Yellow   #
# \[\033[44m\] # Blue     #
# \[\033[45m\] # Purple   #
# \[\033[46m\] # Cyan     #
# \[\033[47m\] # White    #

# High Intensty backgrounds #
# \[\033[0;100m\] # Black #
# \[\033[0;101m\] # Red   #
# \[\033[0;102m\] # Green #

# \[\033[0;103m\] # Yellow#
# \[\033[0;104m\] # Blue  #
# \[\033[10;95m\] # Purple#
# \[\033[0;106m\] # Cyan  #
# \[\033[0;107m\] # White #

#Replace any leading leading 0; with 1; for bold colors#
#Replace any leading 0; with 4; to underline#
#\[\033[32m\]\#

#PS1="|\[\033[36m\]\u\[\033[1m\]@$GREEN\h:\[\033[33;1m\]\w|$RED\$(parse_git_branch)$WHITE\$ "#

PS1="|\[\033[36m\]\u\[\033[33;1m\]\w|$RED\$(parse_git_branch)$WHITE\$ "
