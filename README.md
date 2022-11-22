# whatsapp message without adding a contact

Code for sending a WhatsApp message without storing the contact

On iOS you can create a Safari Favorite using this JavaScript function. When you open this favorite, it will ask you for a phone number.  You can paste the number in, and then it will take you to a new WhatsApp conversation using that number. You won't need to create a contact.

```
javascript:(function(){
var phone = prompt("Who you want to message?", "16185551234").replace(/\D/g,'');
if (phone != null) {
window.location.href = "https://api.whatsapp.com/send?phone=" + phone;
}
})();
```

If you want you can replace the phone number with your own number, so you can send yourself messages easily.  Why would you want to send yourself a message?  Maybe you like talking to yourself. Maybe you want to paste on one device and copy on another one.  :-)

Hat tip to [iDB](https://www.idownloadblog.com/2022/05/26/how-to-message-on-whatsapp-without-saving-contact/) for this code and idea.  I added the ``.replace(/\D/g,'')`` because I wanted to make it more robust, you can paste numbers like ``1-650-555-1234`` or ``1(618)555-1234`` and it will strip out all the non-digits before sending it to the WhatsApp API.  

