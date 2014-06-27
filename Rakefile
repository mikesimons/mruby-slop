task :default do
  mkdir "tmp" if !File.exists? "tmp"
  cd "tmp"
  sh "git clone http://github.com/mikesimons/slop" if !File.exists? "slop"
  cd "slop"
  sh "git checkout mruby"
  sh "git pull"
  sh "cat lib/slop/commands.rb lib/slop/option.rb lib/slop.rb | sed -e '/^require.*/d' > ../../mrblib/slop.rb"
end
