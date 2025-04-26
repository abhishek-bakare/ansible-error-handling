Error handling in Ansible: Lets learn error handling. Consider a below real example a task from project team given to DO
1. Check whether openssl & openssh are installed with latest versions
2. If it is not installed then go to next task
3. Check Docker version
4. If it is not installed then install it

When you see output you can see like this & we can fetch the failed.
```
ok: [13.219.73.74] => {
    "output": {
        "changed": false,
        "cmd": "docker --version",
        "failed": true,    #we used this in when condition
        "msg": "[Errno 2] No such file or directory: b'docker'",
        "rc": 2,
        "stderr": "",
        "stderr_lines": [],
        "stdout": "",
        "stdout_lines": []
    }
}
```
