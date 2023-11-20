##Part 1: Bugs

Given the following buggy code:


`public static int[] reversed(int[] arr) {
    int length = arr.length;
    int[] newArray = new int[length];
    for (int i = 0; i < length; i++) {
        newArray[i] = arr[length - i - 1];
    }
    return newArray;
  }`

A failure-inducing input is as follows:

`import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertArrayEquals;
public class ReversedArrayTest {
    @Test
    public void testReversedFailure() {
        int[] input = new int[]{1, 2, 3, 4, 5};
        int[] expected = new int[]{5, 4, 3, 2, 1};
        assertArrayEquals(expected, ReversedArray.reversed(input));
    }
}`


Likewise, a non-failure-inducing input would be:


`import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertArrayEquals;
public class ReversedArrayTest {
    @Test
    public void testReversedSuccess() {
        int[] input = new int[]{};
        int[] expected = new int[]{};
        assertArrayEquals(expected, ReversedArray.reversed(input));
    }
}`


After the fix, the code looks so:


`public static int[] reversed(int[] arr) {
    int length = arr.length;
    int[] newArray = new int[length];
    for (int i = 0; i < length; i++) {
        newArray[i] = arr[length - i - 1];
    }
    return newArray;
}`


In the original code, the logic is actually correct for reversing the array. The failure-inducing test case should work as expected, reversing the order of the elements in the array. If there is a failure, it might be due to a mistake in the testing setup or the way the ReversedArray.reversed method is being called. The non-failure-inducing input (an empty array) is correctly handled in both the original and fixed versions, as the loop simply doesn't execute when the array length is zero.

##Part 2: The 'less' Command

## 1. Display Line Numbers (`-N` option)
Display line numbers in the `less` command output.

`less -N ./technical/report.txt`

This command displays the contents of report.txt in the ./technical directory with line numbers.

`less -N ./technical/logfile.log`

Here, the logfile.log file is displayed with line numbers, making it easier to reference specific lines. 

URLS: 
1. https://linuxhandbook.com/less-command/#:~:text=,Displaying%20line%20numbers%20in%20less
2. https://linuxize.com/post/less-command-in-linux/

## 2. Finding Text (/pattern)
This command allows you to search for a specific word, phrase, or regex pattern within the file.

`less ./technical/documentation.txt
/error`

After opening documentation.txt, typing /error will highlight occurrences of "error" in the text.

`less ./technical/config.cfg
/timeout`

In this case, searching for "timeout" in config.cfg helps quickly locate relevant configuration settings​​.

URL: https://linuxhandbook.com/less-command/

## 3. Filtering Lines Matching a Pattern (&pattern)

The &pattern option displays only the lines that match a given pattern.

`less ./technical/server.log
&WARNING`

This command filters server.log to only show lines containing "WARNING".

`less ./technical/data.csv
&"2023-01-15"`

Here, data.csv is filtered to display lines that include the date "2023-01-15"​​.

URL: https://linuxhandbook.com/less-command/

## 4.Monitor Files in Real-Time (+F option)

This option allows less to function similarly to tail -f, displaying new lines as they are added to a file.

`less +F ./technical/application.log`

This monitors the application.log file for new entries in real time.

`less +F ./technical/system.log`

Here, system.log is being monitored, showing real-time updates as the system logs new events​​.

URL: https://linuxhandbook.com/less-command/




