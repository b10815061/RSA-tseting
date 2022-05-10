# RSA-testing

this program **is** aimed to validate the encryption part and the decryption part for your RSA algorithm: the program uses p,q,N,phiN,e,d within the ```testcase.txt``` and calls the function wriiten by you to encrypt the plaintext in ```testcase.txt```, if there's no problem with the algorithms, the command prompt should output the plaintext given in ```testcase.txt```. The program also compute the time your algorithm takes to perform pure decrypt compare to using CRT decrypt.

this program **does not** test the validation of key generated by yourself, instead, the key and arguments used in encrypt/decrypt are hard-coded inside the testcast.txt by the author.

# set up the enviroment

```$git pull https://github.com/b10815061/RSA-testing```

the program assumes that you have 

    1.a folder named encrypt containing encrypt.py, which has a main function accepting argument 1,2,3 as msg,N,e, respectively.
    2.a folder named decrypt containing decrypt.py, which has a main function accepting argument 1,2,3 as cipher,N,d, respectively.
    3.a folder named CRT containing CRT.py, which has a main function accepting argument 1,2,3,4 as cipher,p,q,d respectively.

both of the above have a return value returning the result string after computaion(i.e.encrypt/decrypt/CRT).
    
if not, you can modify the code at line 27, line 46, line 71 in test.py so to apply your own funtion.
    
please format your program structure as follow:

```
  RSA-testing
      |--------encrypt
                  |--------encrypt.py
      |--------decrypt
                  |--------decrypt.py
      |--------CRT
                  |--------CRT.py
      .gitignore
      README.md
      test.py
      testcase.txt
```

then, execute the program with 

```$test.py```


# changing the input msg

you can change the input msg manually at line 9 in testcase.

# An example of this program performes

given the plaintext in testcase.txt is : ```*/acbsfrreretrytoencryptME!```

the output of the program : 

```
                                                 ENTERING ENCRYPT PART
MSG =  */acbsfrreretrytoencryptME!
N =  67076433604788366662012044233681513151001167605118830073754993441687362749602150586548487141551016707195948989704061692681509698779783235404702674090889253327573627306136057836618197257324130564662239827736028148973915361236003036427826952835594602031974530096470873595789992841790152854860247192657362632281

EK =  59464218023737817528409320732894954164373232976474221145377330401973451951442714784240397927450038187996398143726479363890607893548269411741907910132057260314131961763169921517026042752308158757906074651989726049374814041452103701028455034164882606605108799923382152164905571136008637493558264750212019344061

ENCRYPTRESULT MGIxMDAwMTAxMTAxMDExMTExMTAxMTEwMDEwMTAwMDAwMTExMTAwMDAwMDAwMTAxMTEwMTEwMDAwMTAxMTAxMDAxMDExMTAwMDEwMTEwMDExMTAwMTEwMDAwMDExMTEwMDExMDExMDEwMTEwMDEwMTEwMDAwMDExMDAwMTAxMTAxMTExMDAwMTExMDExMDAxMDExMDAxMTAxMDAwMDAxMDAwMDExMTExMDExMDEwMTEwMTEwMDExMTAwMDAxMDAxMDEwMTExMTEwMTAwMTEwMDAwMDExMDAwMDExMTExMDExMDExMDExMDExMTAxMDExMTExMDEwMDAwMTEwMTExMTAxMDAwMDEwMDExMTAxMTAxMTAwMDAwMDEwMTAxMTEwMDExMDExMDAxMTAxMTAwMTExMTAwMTExMDExMTAwMDExMDAwMDAxMTAwMDAwMTAwMTAxMDEwMTAxMDAwMTAxMDExMTEwMDAxMTExMTEwMDAxMTEwMTEwMTAxMDAxMTAxMDAxMDAwMTAwMDAxMDAwMTExMTExMDExMTAwMTExMTEwMTAxMDEwMTAxMTAxMDAxMDEwMTEwMTEwMTAwMTAwMTAwMDAwMTAwMDExMDAxMTAwMTAxMDExMDExMTAxMDEwMTAwMDAwMDEwMDAxMDAwMTAxMTExMDExMDAwMTExMDAxMTExMDEwMTAwMTAxMTAwMTAwMDExMDExMDEwMTExMDAwMTEwMTAxMDAwMDAwMDAwMDAxMTAxMTExMDExMDEwMDExMDExMTEwMTEwMDExMTAwMDAxMDEwMDAwMTEwMTExMTAxMTAxMDAxMDEwMTAwMTExMTAxMDExMDEwMTAwMTExMDAwMTExMTAwMTAwMDAxMDAwMDEwMDAwMDExMTAwMDAwMTExMTExMTAxMDAwMTEwMDExMTEwMDAwMDAwMDExMDEwMDExMTAwMTAxMDEwMDExMTEwMTAwMDAxMTExMDAwMTAwMDAxMDAxMTAxMTAwMDAwMTAxMDExMTAxMTAwMDAwMDExMDEwMTAxMDExMDExMDExMTAwMDEwMTEwMDAxMDEwMTAxMDAxMDExMTAxMTAwMTEwMTAwMTExMTAxMTExMTAwMTAxMDExMDEwMTExMTExMDExMTEwMDAwMTAwMDAxMTEwMDExMDAxMTEwMDExMDAxMDAwMDEwMDAxMTAwMDEwMTExMTExMTEwMDEwMTAwMTAwMTEwMTExMTAwMTEwMTAxMTAwMDAxMDAxMTAxMTAwMDAwMDAxMDAxMTAxMDEwMTExMDExMDExMTAwMDAxMTAxMDEwMDExMDAxMTAxMDAxMDAwMDAwMDAxMTAxMTExMTExMDAxMTExMTAxMDA
                                                ENTERING DECRYPT PART
N =  67076433604788366662012044233681513151001167605118830073754993441687362749602150586548487141551016707195948989704061692681509698779783235404702674090889253327573627306136057836618197257324130564662239827736028148973915361236003036427826952835594602031974530096470873595789992841790152854860247192657362632281

DK =  4764923263109495806600913344553768524674180756103471680296775602214268793455074855944607867472618510492442375351385002108628333052483451871243888981771181343942277678089652695881445447366975453221894249148987841877797295014790049030819879436939660851738896212362190436230241459082114790480655557261546471433

t1  1652185313.1714213
DECRYPTRESULT */acbsfrreretrytoencryptME!
t2  1652185313.1714213
EXEC TIME  0.0

                                                ENTERING CRT PART
P =  8862798729224077155723380066486269272760350113349135508314663927579632964725255315086182662272973969538809243304561382270223976393085379416974737379118339

Q =  7568312860768394489233174666873892994266349952765720070802718420007456278449191063820349132216633126011504086608519793568268209441229158535207239401726579

DK =  4764923263109495806600913344553768524674180756103471680296775602214268793455074855944607867472618510492442375351385002108628333052483451871243888981771181343942277678089652695881445447366975453221894249148987841877797295014790049030819879436939660851738896212362190436230241459082114790480655557261546471433

t1  1652185313.1870463
CRTRESULT */acbsfrreretrytoencryptME!
t2  1652185313.1870463
EXEC TIME  0.0
```

    

