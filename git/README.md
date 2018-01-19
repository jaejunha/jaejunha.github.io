# git<br>
## "reset" vs "revert"<br>
**reset**<br>
It can clean your log. However, when you use it with other developers, it can cause some conflicts. So, I think it is best to use "git reset" at personal project.<br>
- git reset --hard "log"<br>
  - it can load previous codes, it removes recent work.<br>
- git reset --soft "log"<br>
  - it can load previous codes. However, it does not remove recent work. Instead, recent work will be kept with staged status.<br>
- git reset (--mixed) "log"<br>
  - "--mixed" is optional<br>
  - It is like middle bridge between "--soft" and "--hard". Recent work will be kept with unstaged status.<br>
If you use "git reset" command, then you use "git push 'alias' +'branch'" command.<br>
<br>

**revert**<br>
It reverts codes, and gives a log which contains message related to revert command.<br>
  

