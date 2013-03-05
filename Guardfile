guard :shell do
  watch /.*/ do |m|
  	result = `jasmine-node *.spec.coffee --coffee --verbose --nocolor`
  	puts result
  	n result.gsub /(\n)+/,' '
  end
end

