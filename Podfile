# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'Messenger' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

pod 'FirebaseCore'
pod 'FirebaseDatabase'
pod 'FirebaseAuth'
pod 'FirebaseFirestore'
pod 'GoogleSignIn', '~> 5.0.2'
pod ‘MessageKit’
pod ‘JGProgressHUD’ 
pod ‘RealmSwift’
pod ‘SDWebImage’



  target 'MessengerTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'MessengerUITests' do
    # Pods for testing
  end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
    # some older pods don't support some architectures, anything over iOS 11 resolves that
      config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '12.0'
    end
  end
end

end
