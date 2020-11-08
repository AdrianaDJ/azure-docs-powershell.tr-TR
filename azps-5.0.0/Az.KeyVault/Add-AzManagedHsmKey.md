---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280233"
---
# Add-AzManagedHsmKey

## SYNOPSIS
Yönetilen bir HSM 'de anahtar oluşturur veya bir anahtarı yönetilen bir HSM 'ye aktarır.

## INDEKI

### Interactivecoluştur (varsayılan)
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Interactiveımport
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Inputobjectcreate
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Inputobjectimport
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Resourceıdcreate
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Resourceidmport
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Add-AzManagedHsmKey** cmdlet 'i, yönetilen HSM 'de yönetilen bir HSM 'de anahtar oluşturur veya bir anahtarı YÖNETILEN bir HSM 'ye aktarır.
Aşağıdaki yöntemlerden herhangi birini kullanarak anahtar eklemek için bu cmdlet 'i kullanın:
- Varsayılan anahtar öznitelikleriyle anahtar oluşturma
- Verilen anahtar öznitelikleri ile anahtar oluşturma
- Bilgisayarınızdaki. pfx dosyasından bir anahtar içeri aktarın.
Bu işlemlerden herhangi biri için, anahtar öznitelikleri sağlayabilir veya varsayılan ayarları kabul edebilirsiniz.
Yönetilen HSM 'unuzda varolan bir anahtarla aynı ada sahip bir anahtar oluşturabilir veya içeri aktarırsanız, özgün anahtar yeni anahtar için belirttiğiniz değerlerle güncelleştirilir. Anahtarın söz konusu sürümü için sürüme özgü URI 'yi kullanarak önceki değerlere erişebilirsiniz. Anahtar sürümleri ve URI yapısı hakkında bilgi edinmek için, yönetilen HSM REST API belgelerindeki [anahtarlar ve gizlilikler hakkında](http://go.microsoft.com/fwlink/?linkid=518560) bilgi edinin.

## ÖRNEKLERDEN

### Örnek 1: RSA-HSM anahtarı oluşturma
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

Bu komut testmhsm adlı yönetilen HSM testanahtarındaki TestKey adında bir RSA-HSM anahtarı oluşturur.

### Örnek 2: EC-HSM anahtarı oluşturma
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

Bu komut testmhsm adlı yönetilen HSM testanahtarındaki P-256 eğrisini kullanarak test anahtarı adında bir EC HSM anahtarı oluşturur.

### Örnek 3: varsayılan olmayan değerler içeren bir eki HSM anahtarı oluşturma
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

İlk komut, değerleri çözme ve $KeyOperations değişkeninde doğrulama değerlerini depolar.
İkinci komut, **Get-Date** cmdlet 'INI kullanarak UTC 'de tanımlanmış bir **DateTime** nesnesi oluşturur.
Bu nesne gelecek yıl iki yıl belirtir. Komut bu tarihi $Expires değişkeninde depolar. Daha fazla bilgi için yazın `Get-Help Get-Date` .
Üçüncü komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur. Bu nesne geçerli UTC zamanını belirtir. Komut bu tarihi $NotBefore değişkeninde depolar.
Son komutu, Eki HSM anahtarı olan TestKey adında bir anahtar oluşturur. Komut $KeyOperations depolanan izin verilen anahtar işlemlerinin değerlerini belirtir. Komut, önceki komutlarda oluşturulan *son* ve *notöncesi* parametrelerinin zamanlarını ve yüksek önem düzeyi ve etiket etiketlerini belirtir. Yeni anahtar devre dışı bırakıldı. **Update-AzManagedHsmKey** cmdlet 'ini kullanarak etkinleştirebilirsiniz.

## PARAMETRELERINE

### -CurveName
Eliptik Eğri şifrelemesi 'nin eğri adını belirtir; KeyType EC olduğunda bu değer geçerlidir.

```yaml
Type: System.String
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

### -Devre dışı bırak
Eklediğiniz anahtarın başlangıçtaki durumuna ayarlı olduğunu gösterir.
Anahtarı kullanma girişimleri başarısız olur.
Daha sonra etkinleştirmeyi düşündüğünüz anahtarları önceden yüklüyorsanız, bu parametreyi kullanın.

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

### -Süre sonu
UTC 'de anahtarın son kullanma zamanını belirtir.
Belirtilmezse, anahtarın süresi dolmayacaktır.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmName
HSM adı. Cmdlet, yönetilen bir HSM 'in FQDN 'sini ad ve şu anda seçili olan ortama göre oluşturur.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
HSM nesnesi.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Anahtardosyasıparolası
İçeri aktarılacak anahtar malzemesini içeren yerel dosyanın parolası.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
İçeri aktarılacak anahtar malzemesini içeren yerel dosyanın yolu.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Keyolar
Anahtarla gerçekleştirilebileceği işlemler.
Yoksa tüm işlemler gerçekleştirilebilir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
Bu anahtarın anahtar türünü belirtir.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Anahtar adı.
Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan ve anahtar adından bir anahtarın FQDN 'sini oluşturur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Anahtarın kullanılmadığı UTC saati.
Belirtilmezse, hiçbir sınırlama yoktur.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
HSM kaynak kimliği.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Boyut
RSA anahtar boyutu, bit cinsinden.
Belirtilmezse, hizmet güvenli bir varsayılan olacaktır.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Anahtar etiketleri temsil eden bir Hashtable.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Backup-AzManagedHsmKey](./Backup-AzManagedHsmKey.md)

[Get-AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[Remove-AzManagedHsmKey](./Remove-AzManagedHsmKey.md)

[Geri al-Azmanagedhsmanahtarkaldırma](./Undo-AzManagedHsmKeyRemoval.md)

[Update-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Restore-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)
