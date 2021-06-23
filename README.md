# Saleshandy-Learning
Things I learned as a software engineer at Saleshandy https://www.saleshandy.com/ 

- Isolation of frontend and backend is very important.
- Validation of data should happen at both ends.
- Development of apis should be done while keeping in mind that there is no frontend and user can maliciously use apis.  
- Database access calls should never be in loop ( if possible ).
- To Count with IF condition in MySQL
   round(COUNT(IF( lastOpenedAt <> '0000-00-00 00:00:00', 1, NULL))/COUNT(*) * 100) as 'open',
- Local tunnel to create callback url for testing.
- contact.sequenceContactHistory.forEach((sch, index) => {
          if (!sch.step || !sch.step.sequence) {
            contact.sequenceContactHistory.splice(index, 1);
          }
 });
   // above code has a loop hole, that is, if we are doing forEach and we are calling splice it changes array length but because array length was initially cached the indexing gets disturbed. 
   // Solution: reverse for loop
- Object.freeze()
