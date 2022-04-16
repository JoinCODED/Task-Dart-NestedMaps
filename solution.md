1. First let's iterate over our `list` of `students`:

```dart
  for (Map<String,dynamic> student in students) {
  }
```

2. Now create a variable for `marks` and extract the `marks` list for each `student`:

```dart
  for (Map<String,dynamic> student in students) {
      final marks = student['marks'];
  }
```

3. We need to tell dart that this is a list of integers using the `as` keyword:

```dart
  for (Map<String,dynamic> student in students) {
      final marks = student['marks'] as List<int>;
  }
```

4. Create a variable to store the sum of all marks:

```dart
  for (Map<String,dynamic> student in students) {
      final marks = student['marks'] as List<int>;
      int sum = 0;
  }
```

5. Loop over the list of `marks` and sum all elements:

```dart
  for (Map<String,dynamic> student in students) {
      final marks = student['marks'] as List<int>;
      int sum = 0;
    for (int mark in marks) {
      sum += mark;
    }
  }
```

6. Create a variable and store the average in it:

```dart
final average = sum / marks.length;
```

7. Add the new value we just created to the `student` map under the key of `average`:

```dart
student['average'] = average;
```

8. Finally, print the `student`:

```dart
void main() {
  List<Map<String,dynamic>> students = [
    {
      'name': 'omar',
      'major': 'engineering',
      'marks': [75, 83, 70, 74, 88],
    },
    {
      'name': 'mohammad',
      'major': 'medicine',
      'marks': [95, 82, 89, 98, 85],
    },
    {
      'name': 'salem',
      'major': 'literature',
      'marks': [60, 80, 67, 55, 77],
    },
  ];

    for (Map<String,dynamic> student in students) {
      final marks = student['marks'] as List<int>;
      int sum = 0;
    for (int mark in marks) {
      sum += mark;
    }
    final average = sum / marks.length;
    student['average'] = average;
    print(student);
  }
}
```
