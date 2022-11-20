** Lab Report 5**
```
#set -e

CPATH=".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar"
rm -rf student-submission
git clone $1 student-submission
cd student-submission/
if [[ -f ListExamples.java ]]
then 
    echo ""
else
    echo "Wrong file submitted."
    exit
fi

cd list-examples-grader/
cp student-submission/ListExamples.java ./


javac -cp $CPATH *.java 2> compile-err.txt > out.txt

if [[ $? -eq 0 ]]
then 
    echo ""
else 
    echo "Compile error."
    exit
fi

java -cp $CPATH org.junit.runner.JUnitCore TestListExamples 2> err.txt > out.txt
#grep -c "FAILUTRE!!!" out.txt > result.txt
if [[ $? -eq 0 ]]
then 
    echo "Pass!!!"
    exit
else 
    echo "No Pass!!!"
fi

```
![image](image/lab5-1.png)
![image](image/lab5-2.png)
![image](image/lab5-3.png)

In the third screenshot, grade.sh remove the previous student-submission and clone the new respostudent-submission. Then grade.sh will check if 
the repository contains ListExamples.java. If ListExamples.java is submitted, grade.sh will move ListExamples.java to list-example-grader/, otherwise, it will print out wrong file submitted. In the third scrrenshot, wrong file was submitted, so grade.sh print out "Wrong file submitted."
