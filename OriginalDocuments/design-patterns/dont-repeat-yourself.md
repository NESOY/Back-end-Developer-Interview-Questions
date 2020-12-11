# DRY (Don't Repeat Yourself)

## [Krzysztof Grzybek](https://github.com/krzysztof-grzybek)

DRY 원칙을 위반하는 코드
```javascript
class Employee {
    calculateSalaryNet() {
        return this.hoursWorked * this.hourlyWage;
    }

    calculateSalaryGross() {
        return this.hoursWorked * this.hourlyWage + TAX;
    }
}
```

수정된 코드
```javascript
class Employee {
    calculateSalaryNet() {
        return this.hoursWorked * this.hourlyWage;
    }

    calculateSalaryGross() {
        return this.calculateSalaryNet() + TAX;
    }
}
```
