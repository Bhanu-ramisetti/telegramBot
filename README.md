var TelegramBot = require('node-telegram-bot-api');

var mongojs = require('mongojs');
var cString = "mongodb+srv://bhanusri:bhanusri@cluster0.nao6j.mongodb.net/Onlineclasses?retryWrites=true&w=majority";
var db = mongojs(cString, ['Schedule']);

var token = '1369509660:AAFrYJMWl2bq22y33dlam2tx7QouSAm6QMw';
var bot = new TelegramBot(token, {polling: true});

 bot.on('message', function(msg){
 var d = msg.text;
 var data = d.split(",")
 var A = data[0].toUpperCase()
 var B = data[1].toUpperCase()
 var f ={Branch:A,Day:B}
db.Schedule.find(d, function(err,docs){

	     	if(err){
     		console.log(err)
     	}
     	else{
     		if(A == 'EEE-3' && B == 'MON'){
     		 var index = 1
     		}
               if(A == 'EEE-3' && B == 'TUE'){
     		 var index = 0
     		}
     		if(A == 'EEE-3' && B == 'WED'){
     		 var index = 2
     		}
     		if(A == 'EEE-3' && B == 'THU'){
     		 var index = 3
     		}
     		if(A == 'EEE-3' && B == 'FRI'){
     		 var index = 4
     		}
     		if(A == 'EEE-3' && B == 'SAT'){
     		 var index = 5
     		}
     		if(A == 'IT-3' && B == 'MON'){
     		 var index = 6
     		}
     		if(A == 'IT-3' && B == 'TUE'){
     		 var index = 7
     		}
     		if(A == 'IT-3' && B == 'WED'){
     		 var index = 8
     		}
     		if(A == 'IT-3' && B == 'THU'){
     		 var index = 9
     		}
     		if(A == 'IT-3' && B == 'FRI'){
     		 var index = 10
     		}
     		if(A == 'IT-3' && B == 'SAT'){
     		 var index = 11 
     		}
     		if(A == 'CSE-3' && B == 'MON'){
     		 var index = 12
     		}if(A == 'CSE-3' && B == 'TUE'){
     		 var index = 13 
     		}if(A == 'CSE-3' && B == 'WED'){
     		 var index = 14 
     		}if(A == 'CSE-3' && B == 'THU'){
     		 var index = 15 
     		}
     		if(A == 'CSE-3' && B == 'FRI'){
     		 var index = 16 
     		}
     		if(A == 'CSE-3' && B == 'SAT'){
     		 var index = 17 
     		}
     		if(A == 'ME-3' && B == 'MON'){
     		 var index = 18
     		}
     		if(A == 'ME-3' && B == 'TUE'){
     		 var index = 19
     		}
     		if(A == 'ME-3' && B == 'WED'){
     		 var index = 20
     		}
     		if(A == 'ME-3' && B == 'THU'){
     		 var index = 21
     		}
     		if(A == 'ME-3' && B == 'FRI'){
     		 var index = 22
     		}
     		if(A == 'ME-3' && B == 'SAT'){
     		 var index = 23
     		}
     		if(A == 'CE-3' && B == 'MON'){
     		 var index = 24
     		}
     		if(A == 'CE-3' && B == 'TUE'){
     		 var index = 25
     		}
     		if(A == 'CE-3' && B == 'WED'){
     		 var index = 26
     		}
     		if(A == 'CE-3' && B == 'THU'){
     		 var index = 27
     		}
     		if(A == 'CE-3' && B == 'FRI'){
     		 var index = 28
     		}
     		if(A == 'CE-3' && B == 'SAT'){
     		 var index = 29
     		}
     		if(A == 'ECE-3' && B == 'MON'){
     		 var index = 30
     		}
     		if(A == 'ECE-3' && B == 'TUE'){
     		 var index = 31
     		}
     		if(A == 'ECE-3' && B == 'WED'){
     		 var index = 32
     		}
     		if(A == 'ECE-3' && B == 'THU'){
     		 var index = 33
     		}
     		if(A == 'ECE-3' && B == 'FRI'){
     		 var index = 34
     		}
     		if(A == 'EEE-2' && B == 'SAT'){
     		 var index = 35
     		}
     		if(A == 'EEE-2' && B == 'MON'){
     		 var index = 36
     		}
     		if(A == 'EEE-2' && B == 'TUE'){
     		 var index = 37
     		}
     		if(A == 'EEE-2' && B == 'WED'){
     		 var index = 38
     		}
     		if(A == 'EEE-2' && B == 'THU'){
     		 var index = 39
     		}
     		if(A == 'EEE-2' && B == 'FRI'){
     		 var index = 40
     		}
     		if(A == 'EEE-2' && B == 'SAT'){
     		 var index = 41
     		}
     		if(A == 'IT-2' && B == 'MON'){
     		 var index = 42
     		}
     		if(A == 'IT-2' && B == 'TUE'){
     		 var index = 43
     		}
     		if(A == 'IT-2' && B == 'WED'){
     		 var index = 44
     		}
     		if(A == 'IT-2' && B == 'THU'){
     		 var index = 45
     		}
     		if(A == 'IT-2' && B == 'FRI'){
     		 var index = 46
     		}
     		if(A == 'IT-2' && B == 'SAT'){
     		 var index = 47
     		}
     		if(A == 'CE-2' && B == 'MON'){
     		 var index = 48
     		}
     		if(A == 'CE-2' && B == 'TUE'){
     		 var index = 49
     		}
     		if(A == 'CE-2' && B == 'WED'){
     		 var index = 50
     		}
     		if(A == 'CE-2' && B == 'THU'){
     		 var index = 51
     		}
     		if(A == 'CE-2' && B == 'FRI'){
     		 var index = 52
     		}
     		if(A == 'CE-2' && B == 'SAT'){
     		 var index = 53
     		}
     		if(A == 'ME-2' && B == 'MON'){
     		 var index = 54
     		}
     		if(A == 'ME-2' && B == 'TUE'){
     		 var index = 55
     		}
     		if(A == 'ME-2' && B == 'WED'){
     		 var index = 56
     		}
     		if(A == 'ME-2' && B == 'THU'){
     		 var index = 57
     		}
     		if(A == 'ME-2' && B == 'FRI'){
     		 var index = 58
     		}
     		if(A == 'ME-2' && B == 'SAT'){
     		 var index = 59
     		}
     		if(A == 'CSE-2' && B == 'MON'){
     		 var index = 60
     		}
     		if(A == 'CSE-2' && B == 'TUE'){
     		 var index = 61
     		}
     		if(A == 'CSE-2' && B == 'WED'){
     		 var index = 62
     		}
     		if(A == 'CSE-2' && B == 'THU'){
     		 var index = 63
     		}
     		if(A == 'CSE-2' && B == 'FRI'){
     		 var index = 64
     		}
     		if(A == 'CSE-2' && B == 'SAT'){
     		 var index = 65
     		}
     		if(A == 'ECE-2' && B == 'MON'){
     		 var index = 66
     		}
     		if(A == 'ECE-2' && B == 'TUE'){
     		 var index = 67
     		}
     		if(A == 'ECE-2' && B == 'WED'){
     		 var index = 68
     		}
     		if(A == 'ECE-2' && B == 'THU'){
     		 var index = 69
     		}
     		if(A == 'ECE-2' && B == 'FRI'){
     		 var index = 70
     		}
     		if(A == 'ECE-2' && B == 'SAT'){
     		 var index = 71
     		}
     		if(A == 'CSE-4' && B == 'MON'){
     		 var index = 72
     		}
     		if(A == 'CSE-4' && B == 'TUE'){
     		 var index = 73
     		}
     		if(A == 'CSE-4' && B == 'WED'){
     		 var index = 74
     		}
     		if(A == 'CSE-4' && B == 'THU'){
     		 var index = 75
     		}
     		if(A == 'CSE-4' && B == 'FRI'){
     		 var index = 76
     		}
     		if(A == 'CSE-4' && B == 'SAT'){
     		 var index = 77
     		}
     		if(A == 'EEE-4' && B == 'MON'){
     		 var index = 78
     		}
     		if(A == 'EEE-4' && B == 'TUE'){
     		 var index = 79
     		}
     		if(A == 'EEE-4' && B == 'WED'){
     		 var index = 80
     		}
     		if(A == 'EEE-4' && B == 'THU'){
     		 var index = 81
     		}
     		if(A == 'EEE-4' && B == 'FRI'){
     		 var index = 82
     		}
     		if(A == 'EEE-4' && B == 'SAT'){
     		 var index = 83
     		}
     		if(A == 'CE-4' && B == 'MON'){
     		 var index = 84
     		}
     		if(A == 'CE-4' && B == 'TUE'){
     		 var index = 85
     		}
     		if(A == 'CE-4' && B == 'WED'){
     		 var index = 86
     		}
     		if(A == 'CE-4' && B == 'THU'){
     		 var index = 87
     		}
     		if(A == 'CE-4' && B == 'FRI'){
     		 var index = 88
     		}
     		if(A == 'CE-4' && B == 'SAT'){
     		 var index = 89
     		}
     		if(A == 'ECE-4' && B == 'MON'){
     		 var index = 90
     		}
     		if(A == 'ECE-4' && B == 'TUE'){
     		 var index = 91
     		}
     		if(A == 'ECE-4' && B == 'WED'){
     		 var index = 92
     		}
     		if(A == 'ECE-4' && B == 'THU'){
     		 var index = 93
     		}
     		if(A == 'ECE-4' && B == 'FRI'){
     		 var index = 94
     		}
     		if(A == 'ECE-4' && B == 'SAT'){
     		 var index = 95
     		}
     		if(A == 'ME-4' && B == 'MON'){
     		 var index = 96
     		}
     		if(A == 'ME-4' && B == 'TUE'){
     		 var index = 97
     		}
     		if(A == 'ME-4' && B == 'WED'){
     		 var index = 98
     		}
     		if(A == 'ME-4' && B == 'THU'){
     		 var index = 99
     		}
     		if(A == 'ME-4' && B == 'FRI'){
     		 var index = 100
     		}
     		if(A == 'ME-4' && B == 'SAT'){
     		 var index = 101
     		}
     		if(A == 'IT-4' && B == 'MON'){
     		 var index = 102
     		}
     		if(A == 'IT-4' && B == 'TUE'){
     		 var index = 103
     		}
     		if(A == 'IT-4' && B == 'WED'){
     		 var index = 104
     		}
     		if(A == 'IT-4' && B == 'THU'){
     		 var index = 105
     		}
     		if(A == 'IT-4' && B == 'FRI'){
     		 var index = 106
     		}
     		if(A == 'IT-4' && B == 'SAT'){
     		 var index = 107
     		}

     		bot.sendMessage(msg.chat.id,docs[index].Periods)
     	}
     })

})
