---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94326140"
---
# New-AzADServicePrincipal

## SYNOPSIS
Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur.

## INDEKI

### SimpleParameterSet (varsayılan)

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
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
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### ApplicationObjectWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
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

Yeni bir Azure Active Directory hizmeti sorumlusu oluşturur. Varsayılan parametre kümesi, sağlanmadıysa parametreler için varsayılan değerleri kullanır. Varsayılan değerler hakkında daha fazla bilgi için her parametrenin açıklamasına bakın. Bu cmdlet, **rol** ve **kapsam** parametreleriyle hizmet sorumlusuna rol atama özelliğine sahiptir. İkisi de atlanırsa, katkıda bulunan rol hizmet sorumlusuna atanır. **Rol** ve **kapsam** parametrelerinin varsayılan değerleri geçerli aboneliğin **katkıdır** . Cmdlet, uygulama oluşturur ve ApplicationId sağlanmazsa özelliklerini ayarlar. Uygulamaya özgü parametreleri güncelleştirmek için [Update-AzADApplication](./update-azadapplication.md) cmdlet 'ini kullanın.

> [!WARNING]
> **Yeni-AzADServicePrincipal** komutunu kullanarak bir hizmet sorumlusu oluşturduğunuzda, çıkış, korumanız gereken kimlik bilgilerini içerir. Kodunuzda bu kimlik bilgilerini eklediğinizden veya kaynak denetiminizin kimlik bilgilerini kontrol ettiğinden emin olun. Alternatif olarak, kimlik bilgilerini kullanma gereğini ortadan kaldırmanız için [Yönetilen kimlikler](/azure/active-directory/managed-identities-azure-resources/overview) kullanmayı düşünebilirsiniz.
>
> Varsayılan olarak, **New-AzADServicePrincipal** , [katılımcı](/azure/role-based-access-control/built-in-roles#contributor) rolünü abonelik kapsamındaki hizmet sorumlusuna atar. Güvenliği aşılan hizmet sorumlusunun riskini azaltmak için daha belirli bir rol atayın ve kapsamı kaynak veya kaynak grubuyla daraltın. Daha fazla bilgi için [rol ataması ekleme adımlarını izleyin](/azure/role-based-access-control/role-assignments-steps) .

## ÖRNEKLERDEN

### Örnek 1: basit AD hizmeti sorumlusu oluşturma

Aşağıdaki örnek, belirtilmeyen parametreler için varsayılan değerleri kullanarak bir AD hizmeti sorumlusu oluşturur. Uygulama KIMLIĞI sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturulur. **Rol** veya **kapsam** için değer sağlanmadığı için, oluşturulan hizmet sorumlusuna geçerli aboneliğin **katılımcı** rolü atanır.

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Örnek 2: belirtilen role ve varsayılan kapsama sahip basit AD hizmeti sorumlusu oluşturma

Aşağıdaki örnek, belirtilmeyen parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur. Uygulama KIMLIĞI sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturulur. **Kapsam** parametresi için değer sağlanmadığından, geçerli aboneliğin **okuyucu** izinleriyle hizmet sorumlusu oluşturulur.

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### Örnek 3: belirtilen kapsam ve varsayılan rolle basit AD hizmeti sorumlusu oluşturma

Aşağıdaki örnek, belirtilmeyen parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur. Uygulama KIMLIĞI sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturulur. **Rol** parametresi için değer sağlanmadığından, sağlanan kaynak grubu kapsamının **katılımcı** izinleriyle hizmet sorumlusu oluşturulur.

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Örnek 4: belirtilen kapsam ve rolle basit AD hizmeti sorumlusu oluşturma

Aşağıdaki örnek, belirtilmeyen parametrelerin varsayılan değerlerini kullanarak bir AD hizmeti sorumlusu oluşturur. Uygulama KIMLIĞI sağlanmadığından, hizmet sorumlusu için bir uygulama oluşturulur. Hizmet sorumlusu, sağlanan kaynak grubu kapsamının **okuyucu** izinleriyle oluşturulur.

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Örnek 5: rol atamasıyla uygulama KIMLIĞI 'ni kullanarak yeni bir AD hizmeti sorumlusu oluşturma

Aşağıdaki örnek, uygulama KIMLIĞI ' 00000000-0000-0000-0000-000000000000 ' olan uygulama için yeni bir AD hizmeti sorumlusu oluşturur. **Rol** veya **kapsam** için değer sağlanmadığı için, oluşturulan hizmet sorumlusuna geçerli aboneliğin **katılımcı** rolü atanır.

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Örnek 6: boru kullanarak yeni bir AD hizmeti sorumlusu oluşturma

Aşağıdaki örnek, [Get-AzADApplication](./get-azadapplication.md) cmdlet 'ini kullanarak uygulamayı ' 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' ile alır. Sonuçlar, `New-AzADServicePrincipal` Bu uygulama için yeni BIR ad hizmeti sorumlusu oluşturmak üzere cmdlet 'e verilmez.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### Örnek 7: DisplayName ve parola kimlik bilgilerini kullanarak yeni bir AD hizmeti sorumlusu oluşturma

Aşağıdaki örnek, adı **servicePrincipalName** ve **strongpassworld! 23** adında yeni bir uygulama oluşturur. Oluşturulan uygulama temelinde hizmet sorumlusunu oluşturur. Başlangıç tarihi ve bitiş tarihi parola kimlik bilgilerine eklenir.

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### Örnek 8: DisplayName ve düz anahtar kimlik bilgilerini kullanarak yeni bir AD hizmeti sorumlusu oluşturma

Aşağıdaki örnek, **servicePrincipalName** ve sertifika **$CERT** adlı yeni bir uygulama oluşturur. Oluşturulan uygulama temelinde hizmet sorumlusunu oluşturur. Bitiş tarihi anahtar kimlik bilgilerine eklenir.

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## PARAMETRELERINE

### -ApplicationId

Kiracıdaki bir hizmet sorumlusunun benzersiz uygulama KIMLIĞI. Bu özellik, oluşturulduktan sonra değiştirilemez. Var olan bir uygulama için bir uygulama KIMLIĞI belirtilmemişse uygulama oluşturulur.

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
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue

Asimetrik kimlik bilgileri türü değeri. Base64 Ile kodlanmış sertifikayı temsil eder.

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

### -DisplayName

Hizmet sorumlusunun kolay adı. Bir görünen ad sağlanmadıysa, bu değer varsayılan olarak **Azure-PowerShell-mm-dd-yyyy-ss-dd-ss** değerini alır ve sonek uygulama oluşturma zamanı olur.

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

Kimlik bilgisi kullanımının geçerli bitiş tarihi. Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.
Asimetrik tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten önce veya bu tarihte ayarlanmalıdır.

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
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredential

Uygulamayla ilişkili parola kimlik bilgileri koleksiyonu.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Role

Hizmet sorumlusunun kapsam üzerinde sahip olduğu rol. Değer sağlanmazsa, **rol** varsayılan olarak **katılımcı** rolüne göre ayarlanır.

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

Hizmet sorumlusunun izinleri olan kapsam. Değer sağlanmazsa **, varsayılan olarak** geçerli abonelik kullanılır.

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

Ayarlanırsa, hizmet sorumlusu için varsayılan rol atamasını oluşturmayı atlayın.

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

Kimlik bilgisi kullanımının geçerli başlangıç tarihi. Varsayılan başlangıç tarihi değeri bugün. Asimetrik tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihin üstünde veya sonra olarak ayarlanmalıdır.

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

Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)bakın.
## GÖLGELENDIRICI

### System. Guid

### System. String

### Microsoft. Azure. Commands. ActiveDirectory. PSADApplication

### Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []

### Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []

### System. DateTime

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal

### Microsoft. Azure. Commands. resources. modeller. Authorization. PSADServicePrincipalWrapper

## NOTLARıNDA

Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[Yeni-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)