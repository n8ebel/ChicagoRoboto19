# Make it more obvious that a PR is a work in progress and shouldn't be merged yet
warn("PR is classed as Work in Progress") if github.pr_title.include? "[WIP]"

message "Thanks @#{github.pr_author} 👍👍"

warn("You should provide a summary in the Pull Request description so that the reviewer has more context on this Pull Request 🤔") if github.pr_body.length < 5

#
# Notify of the release APK size.
#
apk_size = (File.size('app/build/outputs/apk/release/app-release-unsigned.apk').to_f / 2**20).round(2)
message "Release APK size: #{apk_size} MB"