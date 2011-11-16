require 'guard'

guard 'rspec', :version => 2, :cli => '--color', :all_on_start => false, :all_after_pass => false do
  watch('spec/spec_helper.rb')  { "spec" }

  watch(%r{(?:^|\/)spec/.+_spec\.rb$})
  watch(%r{(?:^|\/)spec/helpers/(.+)\.rb$})
  watch(%r{(?:^|\/)app/(.+)\.rb$})                           { |m| "spec/#{m[1]}_spec.rb" }
  watch(%r{(?:^|\/)lib/(.+)\.rb$})                           { |m| "spec/lib/#{m[1]}_spec.rb" }
  
  watch(%r{^spec/factories/(.+)\.rb$})
end

guard 'bundler' do
  watch('Gemfile')
end