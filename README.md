# Ansible-Jinja casting problem POC
---
When creating variable inside tasks, even using "|int" filter, result
passed to jinja is still string. POC consists of :
- Task that generates two variables
   - Just |length filter, which should return int
   - Casted inside tasks
- Two templates
   - casting_test.txt.j2 - Parses and runs, but not as expected in every line
   - casting_test_fails.txt.j2 - Fails during parsing 
- Successful generation result in  result/casting_test.txt
 
