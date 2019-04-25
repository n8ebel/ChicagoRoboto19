# Make it more obvious that a PR is a work in progress and shouldn't be merged yet
warn("PR is classed as Work in Progress") if github.pr_title.include? "[WIP]"

message "Thanks @#{github.pr_author} 👍👍"

#
# Notify of the release APK size.
#
apk_size = (File.size('app/build/outputs/apk/release/app-release-unsigned.apk').to_f / 2**20).round(2)
message "Release APK size: #{apk_size} MB"