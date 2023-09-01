# Uncomment the next line to define a global platform for your project
platform :ios, '9.0'

post_install do | installer |
  installer.generated_projects.each do |project|
    project.targets.each do |target|
      target.build_configurations.each do |config|
        if config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'].split('.').first.to_i < 11
          config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '11.0'
        end
      end
    end
  end
end

target 'DiscoverSQLite' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  pod 'SQLite.swift/SQLCipher', '~> 0.14.0'

  # Pods for DiscoverSQLite

end
