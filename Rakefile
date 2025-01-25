# frozen_string_literal: true

require 'asciidoctor-diagram'
require 'asciidoctor-revealjs'

task :default do
  Asciidoctor.convert_file('presentation.adoc',
                           backend: 'revealjs',
                           safe: Asciidoctor::SafeMode::UNSAFE,
                           to_dir: 'build',
                           mkdirs: true)
  FileUtils.cp_r('images', 'build') if File.exist?('images')
end
