```asm
section .data
   name       db "João Gustavo", 0xA, 0xD
   country    db "Brazil", 0xA, 0xD
   email      db "jgbispo20@gmail.com", 0xA, 0xD
   website    db "https://bispolink.vercel.app/", 0xA, 0xD
   skills     db "Node.js", "React.js", "CSharp", "C", "Java", "Assembly"  
   interests  db "Game Development", "Web evelopment", "Security"
  
section .text
  global _start

  _start:
    mov ecx, name
    call _print
    
    mov ecx, country
    call _print
    
    mov ecx, email
    call _print
    
    mov ecx, website
    call _print
    
    mov ecx, skills
    call _print
    
    mov ecx, interests
    call _print
  
  _print:
    call _calcSizeOfString
    mov eax, 0x1
    mov ebx, 0x1
    int 0x80
    ret
    
  _calcSizeOfString:
    mov edx, ecx
    .nextChar:
      cmp byte[edx], null
      jz endLoop
      jmp .nextChar
  
  _endLoop
    sub edx, ecx
    ret
    
  _end:
    mov eax, 0x1
    mov ebx, 0x0
    int 0x80
```
