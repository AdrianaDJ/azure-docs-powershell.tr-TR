---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105970"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
Sunucu bağlantı bağlamı oluşturur.

## INDEKI

### ByServerNameWithSqlAuth (varsayılan)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-Azuressqldatabaseservercontext** cmdlet 'ı Azure SQL veritabanı sunucusu bağlantı bağlamı oluşturur.
Belirtilen kimlik bilgilerini kullanarak SQL veritabanı sunucusuna bağlantı bağlamı oluşturmak için SQL Server kimlik doğrulamasını kullanın.
SQL veritabanı sunucusunu ad veya URL ile belirtebilirsiniz.
Kimlik bilgilerini almak için, Kullanıcı adını ve parolayı belirtmenizi isteyen Get-Credential cmdlet 'ini kullanın.

Belirtilen Azure aboneliği verilerini kullanarak belirtilen SQL veritabanı sunucusuna bir bağlantı bağlamı oluşturmak için, sertifika tabanlı kimlik doğrulama ile **Yeni-Azuressqldatabaseservercontext** cmdlet 'ini kullanın.
SQL veritabanı sunucusunu ada göre veya tam adı ile belirtebilirsiniz.
Abonelik verilerini parametre olarak belirtebilirsiniz veya geçerli Azure aboneliğinden alınabilir.
https://msdn.microsoft.com/library/windowsazure/jj152833.aspxGeçerli Azure aboneliğini seçmek Için Select-azuyeniden

## ÖRNEKLERDEN

### Örnek 1: SQL Server kimlik doğrulamasını kullanarak bağlam oluşturma
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Bu örnekte SQL Server kimlik doğrulaması kullanılmaktadır.

İlk komut sizden Sunucu Yöneticisi kimlik bilgilerini sorar ve $Credential değişkeninde kimlik bilgilerini depolar.

İkinci komut, $Credential kullanarak lpqd0zbr8y adlı SQL veritabanı sunucusuna bağlanır.

Son komut, $Context içeriğin parçası olan sunucuda Database17 adlı bir veritabanı oluşturur.

### Örnek 2: sertifika tabanlı kimlik doğrulaması kullanarak bağlam oluşturma
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

Bu örnekte sertifika tabanlı kimlik doğrulama kullanılmaktadır.

İlk iki komut $SubscriptionId ve $Thumbprint değişkenlerine değerler atar.

Üçüncü komut $Thumbprint 'da parmak iziyle tanımlanan sertifikayı alır ve $Certificate depolar.

Dördüncü komut, aboneliği Subscription07 olarak ayarlar ve beşinci komut bu aboneliği seçer.

Son komutu, lpqd0zbr8y adlı sunucudaki geçerli abonelikte bir bağlam oluşturur.

## PARAMETRELERINE

### -Credential
Sunucuya erişmeniz için SQL Server kimlik doğrulamasını sağlayan bir kimlik bilgisi nesnesi belirtir.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tamyqualifiedservername
Azure SQL veritabanı sunucusu için tam etki alanı adı (FQDN) adını belirtir.
Örneğin, Server02.database.windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
Bu cmdlet 'in sunucunun Azure SQL DatabaseManagement portalına kullandığı URL 'YI belirtir.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Veritabanı sunucusunun adını belirtir.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Bu cmdlet 'in bağlantı bağlamını oluşturmak için kullandığı Azure aboneliğinin adını belirtir.
Bu parametre için bir değer belirtmezseniz, cmdlet geçerli aboneliği kullanır.
Geçerli aboneliği değiştirmek için Select-AzureSubscription cmdlet 'ini çalıştırın.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
Bu cmdlet 'in bağlantı bağlamını oluşturmak için Azure aboneliğini kullandığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. IServerDataServiceContext

## NOTLARıNDA
* Etki alanı belirtmeden kimlik doğrulatın ve Windows PowerShell 2,0 kullanıyorsanız, Get-Credential cmdlet 'i bir ters eğik çizgi () döndürür; \\ Örneğin, Kullanıcı1. Windows PowerShell 3,0 ters eğik çizgiyi eklemez. Bu ters eğik çizgi, **New-Azuressqldatabaseservercontext** cmdlet 'inin *Credential* parametresi tarafından tanınmaz. Kaldırmak için, aşağıdakine benzer komutları kullanın:

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı cmdlet 'Leri](./Azure.SQLDatabase.md)

[Get-Azuressqldatabase](./Get-AzureSqlDatabase.md)

[Yeni-Azuressqldatabase](./New-AzureSqlDatabase.md)

[Remove-Azuressqldatabase](./Remove-AzureSqlDatabase.md)

[Set-Azuressqldatabase](./Set-AzureSqlDatabase.md)


