FY Calendar Plugin Documentation

Plugin Properties & Methods.

1)	fyData 
2)	selectedYear 
3)	selectedMonth
4)	calendarType
5)	getMonth
6)	getYear
7)	setQtr
8)	getDefaultDate 

How to use these methods & properties:-

fyData – In fyData we have to pass Json format data to generate calendar accordingly.

selectedYear – selectedYear is optional if we not pass any value then it will take current financial year, in selectedYear we can set default financial year or we can pass data dynamically.
selectedMonth – selectedMonth is optional if we not pass any value then it will take current month, in selectedMonth we can set default Month or we can pass data dynamically.
calendarType – calendarType is used to set the type of calendar, I should be monthly or quarterly.
getMonth – It is use to get month value whenever you click on any month.
getYear – It is use to get financial year on dropdown selection.
setQtr – setQtr returns value it should be quarter or month on selection of financial year, according that is generating calendar.
getDefaultDate – It is use to get Default financial year and month on load of calendar. 


Example : -  




$('.fy_calendar').financialCalendar({

        fyData: fyCalData,
        
        selectedYear: '2018-19',
        
        selectedMonth: '09',
        
        calendarType: 'Q',
        
        getMonth: function(m){
            console.log(m);
        },
        
        getYear: function(y){
            console.log(y);
        },
        
        setQtr: function(){
        
            if(fy =='2017-18'){
                return 'Q';
            } else if(fy =='2018-19'){
                return 'M';
            } else{
                return 'M';
            }

        },
        getDefaultDate: function(d){
            console.log(d);
        }
    });

})
