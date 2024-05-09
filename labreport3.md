![20613eff68f0f33f4fef8f9c6967e9e8](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/d78abf83-d084-44cf-a0c9-e575611baac5)

![613787f64e27c1a066a5352428ebc251](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/9edc8729-a2a6-48a1-9119-0b9dd553b80a)

find technical -type f -name "chapter*"

Explanation:
This command searches for all files within the technical directory that start with "chapter" in their names. It is particularly useful for quickly locating all chapter-related documents within the 9/11 report section, assisting in efficient document management or review processes

find technical -type f -name "1468-6708*"

Explanation:
Similar to the first, this command locates all files in the technical/biomed directory that begin with "1468-6708," which seems to be a specific identifier possibly related to journal entries or research papers. This approach helps in pinpointing specific studies or documentation relevant to ongoing biomedical research or audits.
____

![9407c82cde478a9c23fb8581e145ec76](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/2de2f826-3f20-4e65-9019-078b4427aa92)


![da54c62c3c195d95a3cea8a8dba64b16](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/b4e12a4a-19fb-434d-9d13-1ccfc78feb7b)

find ./technical/biomed -type f -mtime -30

Explanation:
This command searches for all files (-type f) in the ./technical/biomed directory that were modified within the last 30 days (-mtime -30), providing a list of such files to ensure recent changes are tracked or updated.

find ./technical/government -type f -mtime -30

Explanation:
Similar to the first, this command locates all files in the ./technical/government directory that have been modified in the last 30 days, useful for monitoring recent document updates or modifications in government-related projects.

_______


![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/25878160-114e-44c7-a253-5554febf4d9e)

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/2e1e60df-b897-4fe7-9562-fe8701aa475b)

find ./technical/biomed -type f -name "1471-213X-*.txt"

Explanation:
This command is used to locate all files within the technical/biomed directory that start with the identifier "1471-213X-" and end with the .txt extension. It appears to target a series of text files, possibly representing serialized journal articles or study data pertinent to biomedical research. This is useful for organizing or processing specific research outputs within a larger collection.

find ./technical/government -type f \( -name "*report*.txt" -o -name "*summary*.doc" \)

Explanation:
This command searches for files within the technical/government directory that either contain "report" in their .txt filename or "summary" in their .doc filename. This is particularly beneficial for retrieving a variety of document types related to governmental reports and summaries, aiding in the easy access of administrative or legislative documents necessary for review or compliance checks.
______

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/fffa1b1c-cae2-4b77-b0ee-1c2cdd2500f7)


![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/5cc60f08-bd93-4ada-a3a8-10a433c67a80)

find ./technical -type f -regex ".*\.\(txt\|log\)" | head -n 5

Explanation:
This command searches the technical directory for files with names ending in .txt or .log using a regular expression. The use of head -n 5 limits the output to the first five results, making it easier to manage and review a small, representative sample of the files.

find ./technical -type f -regex ".*\.\(txt\|pdf\)" | head -n 5

Explanation:
Similarly, this command looks for files ending in .txt or .pdf within the technical directory, employing a regular expression for pattern matching. The head -n 5 command again trims the output to only the first five entries, providing a quick snapshot of the existing document types without overwhelming the user with too much data at once.
Both commands are useful for swiftly locating specific types of documents within a large directory structure, helping to streamline file management tasks or audits that require attention to document formats.









Bibliography
________
"Find Command in Linux." Snapshooter, https://snapshooter.com/learn/linux/find. Accessed [5/8/24].





____

PART 1 

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/fb861137-aff0-4284-9e23-70366e0b0c64)
Failure

![image](https://github.com/markymarkatbb/cse15l-lab-reports/assets/156377140/2ea3a612-26d9-4cb0-963e-1c4512ab2a07)
Passed the test

Explanation:
Bug in reverseInPlace(int[] arr): The original method incorrectly attempted to reverse the array by directly assigning values without temporarily storing one of them, leading to an overwrite and incorrect results. Fix: I introduced a temporary variable to safely swap the values without loss, ensuring the array is accurately reversed in-place.
Bug in reversed(int[] arr): Initially, this method incorrectly modified the original array instead of filling the new array with reversed values. Fix: I adjusted the method to correctly populate a new array (newArray) with the reversed order of elements from the original array (arr), returning this new array without altering the original.
