
var countDownDate = new Date("Feb 12, 2023 00:00:00").getTime();

var x = setInterval(function() {
  var now = new Date().getTime();

  var distance = countDownDate - now;

  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  document.getElementById("countdown-clock").innerHTML = days + "d " + hours + "h "
  + minutes + "m " + seconds + "s ";

  if (distance < 0) {
    clearInterval(x);
    document.getElementById("countdown-clock").innerHTML = "EXPIRED";
  }
}, 1000);


function bookATrip() {
  var firstName = prompt("Podaj imię: ");
  var lastName = prompt("Podaj nazwisko: ");
  var phoneNumber = prompt("Podaj nr telefonu: ")

  if(firstName != null && lastName !=null && phoneNumber !=null){
    document.getElementById("book-a-trip").innerHTML = "Wycieczka została zarezerwowwana. Dziękujemy!"
  }
}