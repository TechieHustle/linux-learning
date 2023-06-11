#### Command Redirections
> cmd > output.log 2>&1 & OR cmd &> output.log
> - Here, the stdout output is redirected to output.log file by first ">", and 2>&1 redirects the error to the same output. 
> - "2" represents stderr file descriptor, while "1" is stdout file descriptor, so &1 means location of stdout, which in this case is output.log
> Example (& at the end runs the command in background): ping -c5 8.8.8.8 >output.log 2>&1 &
