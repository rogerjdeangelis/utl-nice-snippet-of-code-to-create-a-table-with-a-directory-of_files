# utl-nice-snippet-of-code-to-create-a-table-with-a-directory-of_files
Nice snippet of code to create a table with all file anmes in a folder 
    Nice snippet of code to create a table with all file anmes in a folder                                                    
                                                                                                                              
    github                                                                                                                    
    https://tinyurl.com/r6flbpd                                                                                               
    https://github.com/rogerjdeangelis/utl-nice-snippet-of-code-to-create-a-table-with-a-directory-of_files                   
                                                                                                                              
    https://tinyurl.com/tq88kqy                                                                                               
    https://communities.sas.com/t5/SAS-Programming/Requesting-ideas-to-efficiently-read-multiple-external-files/m-p/610069    
                                                                                                                              
    Ksharp                                                                                                                    
    https://communities.sas.com/t5/user/viewprofilepage/user-id/18408                                                         
                                                                                                                              
    *_                   _                                                                                                    
    (_)_ __  _ __  _   _| |_                                                                                                  
    | | '_ \| '_ \| | | | __|                                                                                                 
    | | | | | |_) | |_| | |_                                                                                                  
    |_|_| |_| .__/ \__,_|\__|                                                                                                 
            |_|                                                                                                               
    ;                                                                                                                         
                                                                                                                              
    data _null_;                                                                                                              
                                                                                                                              
    file "d:/tmp/file1.txt";                                                                                                  
    put "d:/tmp/file1.txt";                                                                                                   
                                                                                                                              
    file "d:/tmp/file2.txt";                                                                                                  
    put "d:/tmp/file2.txt";                                                                                                   
                                                                                                                              
    file "d:/tmp/file3.txt";                                                                                                  
    put "d:/tmp/file3.txt";                                                                                                   
    stop;                                                                                                                     
                                                                                                                              
    run;quit;                                                                                                                 
                                                                                                                              
    %let dir='d:/tmp';                                                                                                        
                                                                                                                              
     Directory of d:\tmp                                                                                                      
                                                                                                                              
    12/07/2019  10:07 AM    <DIR>          .                                                                                  
    12/07/2019  10:07 AM    <DIR>          ..                                                                                 
    12/07/2019  10:01 AM                18 file1.txt                                                                          
    12/07/2019  10:01 AM                18 file2.txt                                                                          
    12/07/2019  10:01 AM                18 file3.txt                                                                          
                                                                                                                              
                   3 File(s)             54 bytes                                                                             
                                                                                                                              
                   2 Dir(s)  845,992,239,104 bytes free                                                                       
                                                                                                                              
    *            _               _                                                                                            
      ___  _   _| |_ _ __  _   _| |_                                                                                          
     / _ \| | | | __| '_ \| | | | __|                                                                                         
    | (_) | |_| | |_| |_) | |_| | |_                                                                                          
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                         
                    |_|                                                                                                       
    ;                                                                                                                         
                                                                                                                              
    WORK.DIRECTORY total obs=3                                                                                                
                                                                                                                              
          FILENAME                                                                                                            
                                                                                                                              
      d:/tmp/file1.txt                                                                                                        
      d:/tmp/file2.txt                                                                                                        
      d:/tmp/file3.txt                                                                                                        
                                                                                                                              
    *                                                                                                                         
     _ __  _ __ ___   ___ ___  ___ ___                                                                                        
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|                                                                                       
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                                       
    | .__/|_|  \___/ \___\___||___/___/                                                                                       
    |_|                                                                                                                       
    ;                                                                                                                         
                                                                                                                              
    %let dir=d:/tmp/;                                                                                                         
                                                                                                                              
    data directory;                                                                                                           
      _nam=filename('fid',"&dir");                                                                                            
      _opn=dopen('fid');                                                                                                      
      do _n_=1 to dnum(_opn);                                                                                                 
         filename="&dir./"!!dread(_opn,_n_);                                                                                   
         output;                                                                                                              
         drop _:;                                                                                                             
      end;                                                                                                                    
    run;quit;                                                                                                                 
                                                                                                                              
                                                                                                                              
