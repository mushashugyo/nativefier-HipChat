APP_NAME=武者修行Adv1
APP_PATH=$(APP_NAME)-darwin-x64/$(APP_NAME).app

all: $(APP_PATH)

icon.icns: $(wildcard icon.iconset/*.png)
	iconutil -c icns icon.iconset

$(APP_PATH): icon.icns
	nativefier --icon $< --app-name "$(APP_NAME)" "https://mushashugyo-adv-1.hipchat.com/chat"
