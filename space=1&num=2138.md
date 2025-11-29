```cpp
#include <bits/stdc++.h>
using namespace std;

void fix_IO()
{
    ios_base::sync_with_stdio(0);
    cin.tie(0);
    cout.tie(0);
}

void file_STD(const string& file_Name = "")
{
    const string INP_File = file_Name + ".INP";
    const string OUT_File = file_Name + ".OUT";
    if (fopen(INP_File.c_str(), "r"))
    {
        freopen(INP_File.c_str(), "r", stdin);
        freopen(OUT_File.c_str(), "w", stdout);
    }
}

string type;
unsigned int v;

void read_Data()
{
    cin >> type >> v;
}

void Solve()
{
    if (type == "GOOD")
    {
        cout << (v & 0xFF) * 256*256*256 + ((v >> 8) & 0xFF) * 256*256 + ((v >> 16) & 0xFF) * 256 + ((v >> 24) & 0xFF);
    }
    else
    {
        cout << ((v >> 24) & 0xFF) + ((v >> 16) & 0xFF) * 256 + ((v >> 8) & 0xFF) * 256*256 + (v & 0xFF) * 256*256*256;
    }
}

int main()
{
    fix_IO();
    file_STD("tgtbatu");
    read_Data();
    Solve();
    return 0;
}

/*
[Info]
Akira Kaito | Handle: akirakaitoac
Tui La No Mo Ka | Handle: tuilanomoka
[Info]
*/
```
