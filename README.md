# SCSpecs

添加Spec Repo

$ pod repo add SCSpecs https://github.com/JianlinZhu/SCSpecs.git


本地测试podspec文件

 platform :ios, '7.0'
 
 pod 'PodTestLibrary', :path => ‘../../SCUtility’      		#指定路径

 pod 'PodTestLibrary', :podspec => '../../SCUtility.podspec'  	#指定podspec文件


向Spec Repo提交podspec

$ pod repo push SCSpecs SCUtility.podspec


使用制作好的Pod

$ pod ‘SCUtility’, '~> 1.0.0’


更新维护podspec

$ git push origin master     			#修改更新完成提交到远端仓库

$ git tag -m “new update release" “1.1.0”

$ git push --tags     				#推送tag到远端仓库

$ pod lib lint 					#编辑podspec文件并验证通过

$ pod repo push SCSpecs SCUtility.podspec	#提交到Spec Repo
