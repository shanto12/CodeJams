
# input() reads a string with a line of input, stripping the '\n' (newline) at the end.
# This is all you need for most Code Jam problems.


# https://code.google.com/codejam/contest/dashboard?c=32003

t = int(input())  # read a line with a single integer
print(' ')
for t_case in range(1, t + 1):
    al_number, source_lang, targ_lang = input().split(" ")  # read a list of integers, 2 in this case

    source_length = len(source_lang)
    source_pos_dict = {}
    for i, char in enumerate(source_lang):
        source_pos_dict[char] = i

    iter_count = 0
    for i, char in enumerate(reversed(al_number)):
        iter_count += source_pos_dict[char]*(source_length ** i)

    # Done upto here



    # Convert to target

    target_length = len(targ_lang)
    target_index_dict = {}
    for i, char in enumerate(targ_lang):
        target_index_dict[i] = char

    result = ''

    pos_len = 0
    while iter_count>(target_length**pos_len-1):
        pos_len += 1

    for i in reversed(range(pos_len)):
        for j in reversed(range(target_length)):
            if j * (target_length**i)<=iter_count:
                result += target_index_dict[j]
                iter_count -= j * (target_length**i)
                break
        # else:
        #     result += target_index_dict[0]





    print("Case #{}: {}".format(t_case, result))
