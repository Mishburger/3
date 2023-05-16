#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
using namespace std;
int main() 
{
    vector<string> words = {"bella", "label", "roller"};
    vector<char> result;

    sort(words.begin(), words.end());

    set_intersection(words[0].begin(), words[0].end(),
                          words[1].begin(), words[1].end(),
                          back_inserter(result));

    set_intersection(words[2].begin(), words[2].end(),
                          result.begin(), result.end(),
                          back_inserter(result));

    for (auto c : result) 
        cout << c << ' ';
    cout << endl;
 
    return 0;
}
