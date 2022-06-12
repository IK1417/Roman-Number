class RomanNumerals:

    def to_roman(val):
        result = ''
        i = 0
        a = [['', 'I', 'II', 'III', 'VI', 'V', 'IV', 'IIV', 'IIIV', 'XI'],
             ['', 'X', 'XX', 'XXX', 'LX', 'L', 'XL', 'XXL', 'XXXL', 'CX'],
             ['', 'C', 'CC', 'CCC', 'DC', 'D', 'CD', 'CCD', 'CCCD', 'MC'], ['', 'M', 'MM', 'MMM']]
        while val != 0:
            result += a[i][val % 10]
            i += 1
            val //= 10
        return result[::-1]

    def from_roman(roman_num):
        alph = ['I', 'V', 'X', 'L', 'C', 'D', 'M']
        result = 0
        ones = ['I', 'X', 'C']
        a = {
        'I': 1,
        'V': 5,
        'X': 10,
        'L': 50,
        'C': 100,
        'D': 500,
        'M': 1000,
        }
        for i in range(len(roman_num)):
            word = roman_num[i]
            if word in ones:
                try:
                    if alph[alph.index(roman_num[i + 1]) - 2] == word or alph[alph.index(roman_num[i + 1]) - 1] == word:
                        result -= a[word] * 2
                except IndexError:
                    pass
            result += a[word]
        return result
