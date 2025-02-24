
Architecture

Test Case

Leverage

Enhance
## Code Change Loop
### Planner:
1) If the propmpt is not accurate
    Detail steps for migrate, which is different with normal code change
    Target
    which need be changed
2) Knowledge for code change, or it is not correct will be dead after loops

3) Single agent+tools vs multiple agent 
Single agent will put all function calls in context, the context will be bigger and bigger and agent will forget the initial purpose, like plan
For the single agent, the prompt will be generate plan and code change, which will not be accurate possible

Use multiple agent, the planner agent keep only the planner and each agent keep their context

4) Embedding search is not perfect
    -> see the result of embeding search
    -> how to choose file after search?  
5) Multiple round of interaction
6) as one agent, file content and knowledge will be put in one context， AI will forget the first one 
7) Which the tool be called dependon AI -> Not always called -> plan not always executed -> customer input the build fix
8) accept the agentic concept?
    not repeatable 
    interactive way with human 
    use nature language
9) not possible to solve all issues, interactive with user, this is the right behaviour of migration
10) 15 round, maximu to change 7~8 files
11) a new tools add a new round, more tools , less files



what we can leverage:
1) tools like read and change
2) interaction user experience -> benchmark: config steps

what we can provide
1) code location tools -> enhance embedding
2) code change with knowledge -> need function to call a agent to change the code 
edit agent -> read file -> (return change code??) -> edit file
3) no knowledge base support -> function is not a good way and add more to context


1) more correct than edit agent
2) github server copilot can be integrated with vscode
github extension include agent and skillset

embedding will do only 1 time

## Assessment + Code Chnage Loop
Interate each assessment issue and apply code change


https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/function-calling
https://platform.openai.com/docs/guides/function-calling