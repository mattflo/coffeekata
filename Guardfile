# guard :shell do
#   watch /.*/ do |m|
#   	result = `jasmine-node *.spec.coffee --coffee --verbose --nocolor`
#   	puts result
#   	n result.gsub /(\n)+/,' '
#   end
# end

notification :growl
guard :jasmine, :notifications => true do
  watch(%r{spec/javascripts/spec\.(js\.coffee|js|coffee)$}) { 'spec/javascripts' }
  watch(%r{spec/javascripts/.+_spec\.(js\.coffee|js|coffee)$})
  watch(%r{spec/javascripts/fixtures/.+$})
  watch(%r{app/assets/javascripts/(.+?)\.(js\.coffee|js|coffee)(?:\.\w+)*$}) { |m| "spec/javascripts/#{ m[1] }_spec.#{ m[2] }" }
end
