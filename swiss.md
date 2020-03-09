# H1 Swiss Army Knife


A class that is trying to solve all possible thing that might happen or similar to a master class. A class that is focused on doing many things as opposed to one.

You can recognize a "Swiss Army Knife" if a class is seems to encapsulate too much, or is used in the code as the exclusive class.


An example of a Swiss Army Knife:
```
using System;
namespace DelegateExample {
    public class EmployeeUtils {
        public void FetchEmployeeDetails(string employeeId) {}
        public void SaveEmployeeDetails(EmployeeModel employeeDetails) {}
        public void ValidateEmployeeDetails(EmployeeModel employeeDetails) {}
        public void ExportEmpDetailsToCSV(EmployeeModel employeDetails) {}
        public void ImportEmpDetailsForDb(EmployeeModel employeeDetails) {}
        private class EmployeeModel {
            public string EmployeeId {
                get;
                set;
            }
            public string EmployeeName {
                get;
                set;
            }
            public string EmpplyeeAddress {
                get;
                set;
            }
            public string EmployeeDesignation {
                get;
                set;
            }
            public double EmployeeSalary {
                get;
                set;
            }
        }
    }
}
```

OOP perspectives should adhere to the SOLID mnemonic. One of the keys of Object Oriented languages is abstraction. By failing to break up large classes that are solving multiple issues into small classes that are solving one issue, it becomes a headache to work with and harder to maintain and work on.  Solid says that classes should have a single responsibility. It might seem corollary to not just programming an entire program in main.

The fix is to adhere to OOP design. Abstraction is the key component to this program and the most prudent solution. 
Classes should be broken into their most minimal part while still being functional.


https://sourcemaking.com/antipatterns/swiss-army-knife
