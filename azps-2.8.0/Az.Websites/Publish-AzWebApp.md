---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934286"
---
# Publish-AzWebApp

## SYNOPSIS
Zipdeploy kullanarak bir ZIP, JAR veya WAR dosyasından Azure Web uygulaması dağıtır. 

## INDEKI

### FromResourceName
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromWebApp
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Publish-AzWebApp** cmdlet 'i mevcut bir Azure Web uygulamasına içerik yükler. .NET, Python veya düğüm gibi yığınları kullanıyorsanız veya Java kullanıyorsanız, bir ZIP dosyasında içerik paketlenmesi gerekir. Dağıtım sırasında ek derleme adımları yapılmadan içeriğin önceden oluşturulması ve kullanıma hazır olması gerekir. Bu cmdlet, içeriği dağıtmak için kudu zipdeploy ve wardeploy özelliklerini kullanır. Bir e-posta ile çalışmanın nasıl dağıtılacağı ve bir Web uygulamasının dağıtım için uygun şekilde paketlendirileceklerini öğrenmek için kudu wiki 'ye başvurun. https://aka.ms/kuduzipdeploy ve https://aka.ms/kuduwardeploy zipdeploy ve wardeploy hakkında yararlı ayrıntılar içerir.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

app.zip içeriğini, varsayılan-Web-WestUS kaynak grubuna ait Uygulamam adlı Web uygulamasına yükler.

### Örnek 2
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

Javaproject. war içeriğini, kaynak grubuna ait olan ContosoApp adındaki Web uygulamasının hazırlama yuvasına yükler.

### Örnek 3
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

app.zip içeriğini, ContosoRG kaynak grubuna ait olan ContosoApp adındaki Web uygulamasına yükler. Cmdlet, bir arka plan işinde çalışacaktır.

### Örnek 4
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

Java_app. jar içeriğini, ContosoRG kaynak grubuna ait olan ContosoApp adlı Web uygulamasına yükler.

## PARAMETRELERINE

### -ArchivePath
Arşiv dosyasının yolu. ZIP, WAR ve JAR destekleniyor.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iş
Arka planda cmdlet 'i çalıştırın

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
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

### -Ad
Web uygulamasının adı.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Yuvalı
Web uygulaması yuvasının adı.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebApp
Web App nesnesi

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. WebApps. modeller. PSSite

## ÇıKıŞLAR

### Microsoft. Azure. Commands. WebApps. modeller. PSSite

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
