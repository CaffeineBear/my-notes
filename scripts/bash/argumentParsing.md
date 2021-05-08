# Bash argument parasing

From the medium blog, I found this example where it shows how you
can use case to handle arguments.

```bash
#!/bin/bash
PARAMS=""
while (( "$#" )); do
  case "$1" in
    -a|--my-boolean-flag)
      MY_FLAG=0
      shift
      ;;
    -b|--my-flag-with-argument)
      if [ -n "$2" ] && [ ${2:0:1} != "-" ]; then
        MY_FLAG_ARG=$2
        shift 2
      else
        echo "Error: Argument for $1 is missing" >&2
        exit 1
      fi
      ;;
    -*|--*=) # unsupported flags
      echo "Error: Unsupported flag $1" >&2
      exit 1
      ;;
    *) # preserve positional arguments
      PARAMS="$PARAMS $1"
      shift
      ;;
  esac
done
# set positional arguments in their proper place
eval set -- "$PARAMS"

```

There were also other blogs in Reference section to see more details. The details include: common argument names and etc.


## Common options:

|option | Explanation|
|--- | --- |
| -a | List all items. |
| -c | Get the count of items. |
| -d | Output directory. |
| -e | Expand items. |
| -f | To specify a file. |
| -h | To show the help page. |
| -i | To ignore character case. |
| -l | To list a text. |
| -n | To say no for a question. |
| -o | To sendd output to a file or so. |
| -q | Keep silent; don’t ask the user. |
| -r | To process something recursively. |
| -s | Stealth mode. |
| -v | Verbose mode. |
| -x | Specify executable. |
| -y | To say yes without prompting the user. |


## Reference
- https://medium.com/@Drew_Stokes/bash-argument-parsing-54f3b81a6a8f
- https://likegeeks.com/linux-bash-scripting-awesome-guide-part3/ 
