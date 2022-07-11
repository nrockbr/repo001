#!/bin/bash
# getosversion.sh - Get Hostname, IP and OS Version from a file with IPs
#
# Autor:      Newton Rocha
#
# ------------------------------------------------------------------------ #
#  Example:
#      $ ./os-version.sh myservers_list.txt
# -------------------- VARIABLES ----------------------------------------- #
OUTPUT=server_version.txt
USER=myuser
# -------------------- EXECUTION ----------------------------------------- #
#
while read servers; do
        ssh "$USER@$servers" <<'EOF'
        echo "$(date +%T_%x)" "$(hostname -s)" "$(hostname -I | cut -d " " -f 1)"  "$(uname -a)"
EOF
done < $1 >> $OUTPUT
#
