https://www.youtube.com/watch?v=EHohPpxCMyY
INveritr una lista.
```cpp
ListNode* invertir(ListNode* mipunture){
    ListNode* prev = nullptr;
    ListNode* curr = mipunture;

    while(mipunture != nullptr){
        curr = curr->next;
        mipunture->next = prev;
        prev = mipunture;
        mipunture = curr;
    }
    return prev;
}
```
Otra versión.
```cpp
ListNode* invertir(ListNode* head) {
    ListNode* prev = nullptr;
    ListNode* curr = head;

    while (curr != nullptr) {
        ListNode* next = curr->next; // guardar el siguiente
        curr->next = prev;           // invertir el enlace
        prev = curr;                 // avanzar prev
        curr = next;                 // avanzar curr
    }
    return prev; // nueva cabeza
}
```https://www.youtube.com/watch?v=EHohPpxCMyY