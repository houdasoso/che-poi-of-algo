
# che-poi-of-algo
Algorithm AnalyzeSentence;
    Declare sentence as String;
    Declare length, wordCount, vowelCount as Integer;
    Declare vowels as String = "aeiouAEIOU";
    Declare inWord as Boolean;

Begin
    Display "Enter a sentence ending with a period:";
    Read sentence;

    If sentence does not end with '.' Then
        Display "The sentence must end with a period.";
        Exit;
    End If;

    Set length = 0;
    Set wordCount = 0;
    Set vowelCount = 0;
    Set inWord = False;

    For each character in sentence Do
        Increment length;

        If character is in vowels Then
            Increment vowelCount;
        End If;

        If character = ' ' Then
            Set inWord = False;
        Else If inWord = False Then
            Increment wordCount;
            Set inWord = True;
        End If;
    End For;

    Display "Length of the sentence: ", length;
    Display "Number of words: ", wordCount;
    Display "Number of vowels: ", vowelCount;

End;
