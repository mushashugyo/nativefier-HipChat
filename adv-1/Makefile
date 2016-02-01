APP_NAME=武者修行Adv1
APP_PATH=$(APP_NAME)-darwin-x64/$(APP_NAME).app
EasyWinePATH=/opt/Applications/EasyWine.app/Contents/Resources/wine/bin

all: $(APP_PATH)

icon.icns: $(wildcard icon.iconset/*.png)
	iconutil -c icns icon.iconset

$(APP_PATH): icon.icns
	if ! type wine 2>&1 > /dev/null; then\
		export PATH=$$PATH:$(EasyWinePATH);\
	fi;\
	nativefier --platform win32 --icon $< --app-name "$(APP_NAME)" "https://mushashugyo-adv-1.hipchat.com/chat"


clean:
	rm -rf icon.icns $(dir $(APP_PATH))
	find . -name .DS_Store -delete
