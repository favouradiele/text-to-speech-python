# text-to-speech-python
An app to convert speech to text using only python


Getting started
1. Install the required python packages
pip install pyttsx3
pip install pypiwin32 # Windows only
2. Run the project
python main.py


-t or --text for cli input of text.

python main.py -t "This is input from command line"

-l or --language for cli input of language. Currently it support Hindi and English. Available inputs are english and hindi.
python main.py -t Hello -l english

-a or --accent for cli input of language accent. Only available for english language. Available accents are indian, australian, us and uk. For Hindi it is default set to indian accent.

python main.py -t Hello -l english -a uk
-g or --gender for cli input of voice gender. Available inputs are male and female. By default it is set to male.

python main.py -t Hello -l english -a uk -g female
-i or --index to select rank of the reader form the output list. It starts from 0 (Zero). If you don't select any index it will automatically take the first one.

python main.py -t Hello -l english -a us -g female -i 1

NOTE : Sometimes there might be chances that the readers are not available for specific gender or language or accent. In that case, it tries to find alternative or else it will read by the default reader which has English language, US accent and voice gender is male.

Troubleshooting
OSError: libespeak.so.1: cannot open shared object file: No such file or directory. Install libespeak library in your system. If you're using ubuntu you can do it by sudo apt install libespeak1.

aplay: not found your system needs alsa utils library. If you're on ubuntu you can do it by sudo apt-get install alsa-utils.

aplay: main:788: audio open error: No such file or directory or any other aplay related error. Your system should have soundcard on it. You can check this by aplay -l. As a result of this command if you see something like aplay: device_list:270: no soundcards found... this application will not work for you.

Dependencies
pyttsx3
Contributing
Fork it ( https://github.com/vishalnagda1/text-to-speech/fork )
Create your feature branch (git checkout -b my-new-feature)
Commit your changes (git commit -am 'Add some feature')
Push to the branch (git push origin my-new-feature)
Create a new pull request.
