node {

      stage ('Checkout')

        {

          checkout scm

        }

      stage ('Build')

        {

          bat 'nuget restore WebApplication1.sln'

          bat "\"${tool 'MSBuild'}\" WebApplication1.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"

        }

       stage ('Archive')

       {

        archive 'WebApplication1/bin/Release/**'

       }



   }

