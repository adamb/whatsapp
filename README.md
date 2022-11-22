# whatsapp message without adding a contact

Code for sending a WhatsApp message without storing the contact

On iOS you can create a Safari Favorite using this JavaScript function. When you open this favorite, it will ask you for a phone number.  You can paste the number in, and then it will take you to a new WhatsApp conversation using that number. You won't need to create a contact.

```javascript:(function(){
var phone = prompt("Who you want to message?", "16185551234").replace(/\D/g,'');
if (phone != null) {
window.location.href = "https://api.whatsapp.com/send?phone=" + phone;
}
})();
```

If you want you can replace the phone number with your own number, so you can send yourself messages easily.  Why would you want to send yourself a message?  Maybe you like talking to yourself. :-)
