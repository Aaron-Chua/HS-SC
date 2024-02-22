# HS-SC

The function of this script is to replace the Chinese characters in the Simplified Chinese text entered by the user with other common Chinese characters with the same pronunciation and tone. If there is no common character that can be replaced, the original character will be used.
Each replaced character is preceded and followed by a space. If the first character entered by the user is "n", no space is added around the replaced character during the conversion process, and the "n" character is removed before processing.


## Usage of the script:

Please feel free to use it as you wish!


## The main steps of the script are as follows:

### Initialise the pinyin-to-character mapping: 

Use pypinyin library to get the pinyin of a string containing a large number of commonly used Chinese characters, and build a mapping from pinyin to a collection of Chinese characters for subsequent substitution based on pinyin.

### Define the replacement function:

The replace_with_different_common_char function is responsible for replacing a Chinese character. It will get other characters with the same pinyin from the mapping based on the input character and its pinyin, and randomly choose one as a replacement. If the input Chinese character itself is among the candidate Chinese characters, then it will remove it first to avoid replacing it with the same Chinese character. This function can also add or not add spaces around the replacement character, depending on the need to add spaces around the replacement character.

### Define the convert function:

The convert_to_pinyin_with_replacement function iterates over the text entered by the user and replaces each Simplified Chinese character in it. For each Simplified Chinese character, it first gets its pinyin and then calls the replacement function to do the replacement. Non-Simplified Chinese characters remain unchanged.

### Get user input and set space flag: 

Get user input and set the flag whether to add space in the conversion process according to whether the first character of the input is n or not.

### Execute conversion and output the result: 

Performs the conversion operation and outputs the converted text. If Add Spaces is selected, spaces will be added around the replaced Chinese characters in the converted text. Finally, copy the converted text to the clipboard.


## Shortcomings:

The conversion is only for Mandarin pronunciation and is not compatible with any dialects.

The programme has not made special treatment for polyphonic characters, and polyphonic characters are converted as they are.

There is no GUI.

## Preview:

拣 体 终  闻 的 童  因  惕  唤

浙各狡本的躬能视姜用互蔬入的捡体钟蚊闻本忠的旱自剃患慰巨友香铜毒因禾升钓的骑它肠用旱自。如裹鹊时眉友渴剃贷的尝件自择驶用员自。

美各背剃贷的自钱候君家医各空葛。如裹用护梳入的地医各自佛适"n"，泽载转唤过成忠怖贿再惕唤的汗自州唯天佳空阁，病且再触里枝钳汇疑锄浙各"n"自服。

绞本的用徒：

顷字尤发辉奇用徒
