## Docker

docker stats --format "table {{.Name}}\t{{.CPUPerc}}\t{{.MemUsage}}\t{{.MemPerc}}"

## Launchpad图标大小怎么调整
defaults write com.apple.dock springboard-columns -int 10
defaults write com.apple.dock ResetLaunchPad -bool TRUE;killall Dock
