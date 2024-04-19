// Ask the user for confirmation to take attendance
const userConfirmation = confirm("Do you want to take attendance?");

let userName = "";
let workers = [];
if (userConfirmation) {    
    userName = prompt("Please enter your name:");

        alert(`Welcome, ${userName}! Let's proceed with attendance.`);
}
function takeAttendance(userName) {    
    let attendance = [];
    let signIns = {};
    let work = {};
    let signOuts = {};
    
        let signInTime = prompt(`Enter sign-in time for ${userName} (HH:MM AM/PM)`);    
    signIns[userName] = signInTime;

    let workingdetails = prompt(`Enter your work ${userName} `);    
    work[userName] = workingdetails;  
            
    let signOutTime = prompt(`Enter sign-out time for ${userName} (HH:MM AM/PM)`);    
    signOuts[userName] = signOutTime;   
    return { attendance, signIns,work , signOuts };
}

function manageAttendance() {    
    if (userConfirmation) {        
        let { attendance, signIns,work, signOuts } = takeAttendance(userName);       
    }
}
manageAttendance();
