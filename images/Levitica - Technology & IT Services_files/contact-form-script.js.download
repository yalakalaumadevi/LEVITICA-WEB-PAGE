








$("#contactSendMail").on("click", (e) => {
  e.preventDefault();
  const firstname = document.getElementById("nameInputID").value;
  const email = document.getElementById("email").value;
  const mobile = document.getElementById("phone_number").value;
  const subject = document.getElementById("msg_subject").value;
  const message = document.getElementById("message").value;
  if(firstname == null || firstname == "") {
  alert("please Enter Your name!")
    return;
  } else if(email==null || email == ""){
    alert("please Enter Your email")

    return;
  } else if (mobile==null || mobile==""){
alert("please enter Your mobile number")
    return;
  }else if (subject==null || subject==""){
  alert("please enter your subject")
    return;
  }else if (message==null || message==""){
    alert("please enter your message")
    return;
  }
  console.log(firstname, email, mobile, subject, message);
  let bodyValues = {
    firstname,
    email,
    mobile,
    subject,
    message,
  };
  sendEmail(bodyValues);
});

function sendEmail(bodyValues) {
  let serviceID = "service_4kmq1x9";
  let tempID = "template_m3x0ek8";
  emailjs
    .send(serviceID, tempID, bodyValues)
    .then((res) => {
      console.log("Email sent successfully:", res);
      $(".successErrorMsg").removeClass("d-none alert-danger");
      $(".successErrorMsg").addClass("alert-success");
      $(".successErrorMsg").text("Email sent successfully!");
      // alert("Your message sent successfully");
    })
    .catch((err) => {
      console.error("Email sending error:", err);
      $(".successErrorMsg").removeClass("d-none");
      $(".successErrorMsg").text("Failed to send email. Please try again later.!");
      // alert("Failed to send email. Please try again later.");
    });
}
