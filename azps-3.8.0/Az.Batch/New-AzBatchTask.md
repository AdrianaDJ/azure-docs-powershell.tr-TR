---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 5d2dbd8d8cbb7ca9de264f5d25769a0f0c715730
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107211"
---
# New-AzBatchTask

## SYNOPSIS
Bir iş altında toplu görev oluşturur.

## INDEKI

### JobId_Single (varsayılan)
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobId_Bulk
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Bulk
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### JobObject_Single
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzBatchTask** cmdlet 'ı, *JobId* parametresi veya *iş* parametresi tarafından belirtilen iş altında bir Azure toplu işlemi oluşturur.

## ÖRNEKLERDEN

### Örnek 1: toplu görev oluşturma
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

Bu komut, iş-000001 KIMLIĞI olan işin altında KIMLIK Task23 olan bir görev oluşturur.
Görev belirtilen komutu çalıştırır.
$Context değişkenine bağlam atamak için **Get-AzBatchAccountKey** cmdlet 'ini kullanın.

### Örnek 2: toplu görev oluşturma
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

Bu komut, **Get-AzBatchJob** cmdlet 'ini kullanarak 000001 kimliğine sahip toplu işlemi alır.
Komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.
Komut, iş altında KIMLIK Task26 olan bir görev oluşturur.
Görev, yükseltilmiş izinleri kullanarak belirtilen komutu çalıştırır.

### Örnek 3: ardışık düzeni kullanarak belirtilen işe görev koleksiyonu ekleme
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

İlk komut, **Get-AzBatchAccountKey** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.
Komut bu nesne başvurusunu $Context değişkenine depolar.
Sonraki iki komut, New-Object cmdlet 'ini kullanarak **Ince görev** nesneleri oluşturur.
Komutlar $Task 01 ve $Task 02 değişkenlerinde görevleri depolar.
Final komutu, **Get-AzBatchJob** kullanarak, 000001 kimliğine sahip toplu işlemi alır.
Ardından komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.
Komut bu iş altında bir görev koleksiyonu ekler.
Komut, $Context depolanan bağlamı kullanır.

### Örnek 4: belirtilen işe görevler koleksiyonu ekleme
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

İlk komut, **Get-AzBatchAccountKey** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.
Komut bu nesne başvurusunu $Context değişkenine depolar.
Sonraki iki komut, New-Object cmdlet 'ini kullanarak **Ince görev** nesneleri oluşturur.
Komutlar $Task 01 ve $Task 02 değişkenlerinde görevleri depolar.
Son komut $Task $Task 01 ' de depolanan görevleri, 000001-

### Örnek 5: çıkış dosyalarıyla görev ekleme
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### Örnek 6: kimlik doğrulama belirteci ayarlarıyla görev ekleme
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### Örnek 7: kapsayıcıda çalışan bir görev ekleme
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## PARAMETRELERINE

### -Affinityınformation
Toplu Iş hizmetinin, görevin çalıştırılacağı düğümü seçmek için kullandığı bir konum ipucunu belirtir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Applicationpackagereferfer
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationTokenSettings
Görevin toplu hizmet işlemlerini gerçekleştirmek için kullanabileceği bir kimlik doğrulama belirtecinin ayarları.
Bu ayarlanırsa, toplu hizmet, göreve hesap erişim anahtarı gerekmeden toplu Iş hizmeti işlemlerinin kimliğini doğrulamak için kullanılabilecek bir kimlik doğrulama belirteciyle sağlanır. Belirteç, AZ_BATCH_AUTHENTICATION_TOKEN ortamı değişkeniyle sağlanır. Görevin belirteci kullanarak gerçekleştirebileceği işlemler ayarlara bağlıdır. Örneğin, bir görev projeye başka görevler eklemek için iş izinleri isteyebilir ya da işin veya diğer görevlerin durumunu denetleyebilir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BatchContext
Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.
BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır. Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın. Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır. Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CommandLine
Görevin komut satırını belirtir.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kısıtlamalar
Bu göreve uygulanan yürütme kısıtlamalarını belirtir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerSettings
Görevin çalıştığı kapsayıcının ayarları.
Bu görevi çalıştıran havuzda containerConfiguration ayarlanmışsa, bu da ayarlanmalıdır. Bu görevi çalıştıran havuzda containerConfiguration ayarlanmamışsa, bu ayarlanmamalıdır. Bu belirtildiğinde, tüm dizinler AZ_BATCH_NODE_ROOT_DIR (düğümdeki Azure toplu Iş dizinlerinin kökü) kapsayıcıya eşlenir, tüm görev ortam değişkenleri kapsayıcıya eşlenir ve görev komut satırı kapsayıcıda yürütülür.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bağımlılson
Görevin diğer görevlere bağlı olduğunu belirtir.
Tüm bağlı görevler başarıyla tamamlanıncaya kadar görev planlanmayacaktır.

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Görevin görünen adını belirtir.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentSettings
Anahtar/değer çiftleri olarak, bu cmdlet 'in göreve eklediği ortam ayarlarını belirtir.
Anahtar, ortam ayarı adıdır.
Değer, ortam ayarıdır.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExitConditions
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Görevin KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Bu cmdlet 'in görev oluşturduğu işi belirtir.
Bir **Ince iş** nesnesi edinmek için Get-AzBatchJob cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Bu cmdlet 'in görev oluşturduğu işin KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Multiınstancesettings
Çok örnekli bir görevin nasıl çalıştırılacağı hakkında bilgi belirtir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ÇıktıDosyası
Komut satırını çalıştırdıktan sonra, toplu Iş hizmetinin COMPUTE düğümünden karşıya yükleneceği dosyaların listesini alır veya ayarlar.
Çok örnekli görevler için, dosyalar yalnızca birincil görevin yürütüldüğü işlem düğümünden karşıya yüklenir.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceFiles
Kaynak dosyalarını anahtar/değer çiftleri olarak, görevin gerektirdiği şekilde belirtir.
Anahtar, kaynak dosyası yoludur.
Değer, kaynak dosyası blob kaynağıdır.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Görevler
Eklenecek görevlerin koleksiyonunu belirtir.
Her görevin benzersiz bir KIMLIĞI olmalıdır.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserIdentity
Görevin çalıştığı kullanıcı kimliği.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Get-AzBatchTask](./Get-AzBatchTask.md)

[Yeni-AzBatchTask](./New-AzBatchTask.md)

[Remove-AzBatchTask](./Remove-AzBatchTask.md)

[Stop-AzBatchTask](./Stop-AzBatchTask.md)

[Azure toplu Iş cmdlet 'Leri](/powershell/module/az.batch)


