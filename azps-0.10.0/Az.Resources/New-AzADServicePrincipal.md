---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 96ff12056167adaabcb828e2fedfe0c78d59e963
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94326143"
---
# New-AzADServicePrincipal

## SYNOPSIS
Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.

## INDEKI

### SimpleParameterSet (varsayılan)
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPlainParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithoutCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPlainParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationObjectWithKeyPlainParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur. Kullanıcı için bir değer sağlayamazsa, varsayılan parametre kümesi parametreler için varsayılan değerleri kullanır. Kullanılan varsayılan değerler hakkında daha fazla bilgi için aşağıdaki verilen parametrelerin açıklamasına bakın.
Bu cmdlet, hizmet sorumlusuna ve parametreleriyle rol atama özelliğine sahiptir `Role` `Scope` ; Bu parametrelerden hiçbiri sağlanmadıysa, hizmet sorumlusuna rol atanmaz. `Role`And parametrelerinin varsayılan değerleri `Scope` "katkıda bulunanlar" ve geçerli abonelik, sırasıyla ( _Not_ : yalnızca Kullanıcı iki parametreden biri için bir değer sağlarsa, ancak diğeri yerine bir değer sağlıyorsa kullanılır).
Cmdlet de örtülü olarak bir uygulama oluşturur ve özelliklerini (ApplicationId sağlanmadıysa) ayarlar. Uygulamaya özgü parametreleri güncelleştirmek için lütfen Set-AzADApplication cmdlet 'ini kullanın.

> [!WARNING]
> **Yeni-AzADServicePrincipal** komutunu kullanarak bir hizmet sorumlusu oluşturduğunuzda, çıkış, korumanız gereken kimlik bilgilerini içerir. Kodunuzda bu kimlik bilgilerini eklediğinizden veya kaynak denetiminizin kimlik bilgilerini kontrol ettiğinden emin olun. Alternatif olarak, kimlik bilgilerini kullanma gereğini ortadan kaldırmanız için [Yönetilen kimlikler](/azure/active-directory/managed-identities-azure-resources/overview) kullanmayı düşünebilirsiniz.
>
> Varsayılan olarak, **New-AzADServicePrincipal** , [katılımcı](/azure/role-based-access-control/built-in-roles#contributor) rolünü abonelik kapsamındaki hizmet sorumlusuna atar. Güvenliği aşılan hizmet sorumlusunun riskini azaltmak için daha belirli bir rol atayın ve kapsamı kaynak veya kaynak grubuyla daraltın. Daha fazla bilgi için [rol ataması ekleme adımlarını izleyin](/azure/role-based-access-control/role-assignments-steps) .

## ÖRNEKLERDEN

### Örnek 1-basit AD hizmeti sorumlusu oluşturma

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

Yukarıdaki komut, parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur. Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu. Veya için hiçbir değer sağlanmadığından `Role` `Scope` , oluşturulan hizmet sorumlusunun izinleri yoktur.

### Örnek 2-belirtilen rolle ve varsayılan kapsama sahip basit AD hizmeti sorumlusu oluşturma

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur. Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu. Hizmet sorumlusu, geçerli aboneliğin "okuyucu" izinleriyle oluşturulmuştur (parametre için değer sağlanmadığından beri `Scope` ).

### Örnek 3-belirtilen kapsam ve varsayılan rolle basit AD hizmeti sorumlusu oluşturma

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur. Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu. Hizmet sorumlusu, `Role` sağlanan kaynak grubu kapsamının üzerinde "katkıda bulunanlar" izinleriyle oluşturulmuştur (parametre için değer sağlanmamıştır).

### Örnek 4-belirtilen kapsam ve rolle basit AD hizmeti sorumlusu oluşturma

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

Yukarıdaki komut, sağlanmayan parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur. Uygulama kimliği sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturuldu. Hizmet sorumlusu, sağlanan kaynak grubu kapsamındaki "okuyucu" izinleriyle oluşturulmuştur.

### Örnek 5-rol atamasıyla uygulama kimliği 'ni kullanarak yeni bir AD hizmeti sorumlusu oluşturma

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

Uygulama kimliği ' 34a28ad2-dec2:4-4a41-BC3B-vseç22ddf90000e ' olan uygulama için yeni bir AD hizmeti sorumlusu oluşturur. Veya için hiçbir değer sağlanmadığından `Role` `Scope` , oluşturulan hizmet sorumlusunun izinleri yoktur.

### Örnek 6-Boru kullanarak yeni bir AD hizmeti sorumlusu oluşturma

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

Nesne kimliği ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' ile ve bu uygulama için yeni bir AD hizmeti sorumlusu oluşturmak için New-AzADServicePrincipal cmdlet 'ine sahip olan uygulamayı alır.

## PARAMETRELERINE

### -ApplicationId
Kiracıdaki bir hizmet sorumlusunun benzersiz uygulama kimliği.
Bu özellik, oluşturulduktan sonra değiştirilemez.
Uygulama kimliği belirtilmezse, bir tane oluşturulur.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject
Hizmet sorumlusu 'nın oluşturulduğu uygulamayı temsil eden nesne.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue
"Asimetrik" kimlik bilgileri türü.
Temel 64 kodlu sertifikayı temsil eder.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Hizmet sorumlusunun kolay adı. Bir görünen ad sağlanmadıysa, bu değer varsayılan olarak ' Azure-PowerShell-dd-dd-YYYY-SS-mm-ss ' olarak ayarlanır; burada sonek, uygulama oluşturma zamanı olur.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate
Kimlik bilgisi kullanımının geçerli bitiş tarihi.
Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır. "Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredential
Uygulamayla ilişkili anahtar kimlik bilgileri koleksiyonu.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parola
Hizmet sorumlusu ile ilişkilendirilecek parola. Parola sağlanmadıysa, rastgele bir GUID oluşturulur ve parola olarak kullanılır.

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordCredential
Uygulamayla ilişkili parola kimlik bilgileri koleksiyonu.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Role
Hizmet sorumlusunun kapsam üzerinde sahip olduğu rol. Bir değer `Scope` sağlanmışsa ancak hiçbir değer sağlanmazsa `Role` , `Role` Varsayılan olarak ' katılımcı ' rolü kullanılır.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kapsam
Hizmet sorumlusunun izinleri olan kapsam. Bir değer `Role` sağlanmışsa ancak hiçbir değer sağlanmazsa `Scope` , `Scope` Varsayılan olarak geçerli abonelik kullanılır.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAssignment
Ayarlıysa, hizmet sorumlusu için varsayılan rol atamasını oluşturmayı atlar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate
Kimlik bilgisi kullanımının geçerli başlangıç tarihi.
Varsayılan başlangıç tarihi değeri bugün. "Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. Guid

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication
Parametreler: ApplicationObject (ByValue)

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []

### System. Security. SecureString

### System. DateTime

## ÇıKıŞLAR

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal

### Microsoft. Azure. Commands. resources. modeller. Authorization. PSADServicePrincipalWrapper

## NOTLARıNDA
Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[Yeni-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)

