# Candas2
This is a project inspired on the original Candas library by https://gist.github.com/JulianWgs, a blf file can be handle in a faster way using python data science classical libraries.

#BLF file loading
The CAN file in BLF format is automatically converted into a DataFrame for subsequent processing.
The blf filepath should be provided.

\```python

blf = Candas(r'C:\Users\Folder\file.blf')
\```

\```dart
void main() {
  print(suma());
  print(suma(a: 23, b: 45));

  print(mul());
  print(mul(x: 23, y: 12));
}

int suma({int a = 4, int b = 5}) => a + b;

int mul({int x = 7, int y = 5}) => x * y;
\```


#ID Filtering
IDs are filtered to allow for targeted analysis, ensuring only relevant data is processed.
id_filter --> str

'''
blf.id_filtering(id_filter)
'''

#Time revision between each ID
The time interval between each ID is reviewed to ensure accurate temporal analysis and synchronization.

period_time(int) --> The time period between each ID, measured in milliseconds, is analyzed to ensure precise timing and synchronization in the data.

tolerance(int) --> As with all electronic instruments, a certain level of lag or tolerance is accounted for to ensure accurate data interpretation and analysis. It should be provided in a range from 0 to 100


'''
blf.time_rev(period_time, tolerance)
'''
