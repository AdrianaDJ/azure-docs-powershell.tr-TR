---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571621"
---
# Add-AzureRmAccount

## SYNOPSIS
Azure Resource Manager cmdlet isteklerinde kullanılmak üzere kimliği doğrulanmış bir hesap ekler.

## INDEKI

### Userwithsubscriptionıd (varsayılan)
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UserWithSubscriptionName
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Serviceprincipalwithsubscriptionıd
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionName
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Serviceprincipalcertificatewithsubscriptionıd
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionName
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Accesstokenwithsubscriptionıd
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionName
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Add-AzureRmAcccount cmdlet 'i Azure Resource Manager cmdlet istekleri için kullanılmak üzere kimliği doğrulanmış bir Azure hesabı ekler.

Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager cmdlet 'leriyle kullanabilirsiniz.
Hizmet yönetimi cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesap eklemek için Add-AzureAccount veya Import-AzurePublishSettingsFile cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: etkileşimli oturum açma gerektiren bir hesap ekleme
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

Bu komut bir Azure Resource Manager hesabı ekler.

Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için, istemde, Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgilerini sağlamanız gerekir.

Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.

### Örnek 2: kuruluş KIMLIĞI kimlik bilgileriyle kimlik doğrulaması yapan bir hesap ekleme
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

İlk komut Kullanıcı kimlik bilgilerini alır ve $Credential değişkeninde depolar.

İkinci komut $Credential 'daki kimlik bilgilerine sahip bir Azure Resource Manager hesabı ekler.

Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure Resource Manager ile kimlik bilgilerini doğrular.
Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için Multi-Factor Authentication veya Microsoft hesabı kimlik bilgilerini kullanamazsınız.

### Örnek 3: hizmet sorumlusu kimlik bilgileriyle kimlik doğrulaması yapan bir hesap ekleme
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

İlk komut Kullanıcı kimlik bilgilerini alır ve $Credential değişkeninde depolar.

İkinci komut, belirtilen kiracı için $Credential depolanan kimlik bilgilerine sahip bir Azure Resource Manager hesabı ekler.
ServicePrincipal Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.

### Örnek 4: belirli bir kiracı ve abonelik için hesap ekleme
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

Bu komut, varsayılan olarak belirtilen kiracı ve abonelik cmdlet 'lerini çalıştırmak için bir Azure Kaynak Yöneticisi hesabı ekler.

## PARAMETRELERINE

### -AccessToken
Bir erişim belirteci belirtir.

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
Erişim belirtecinin hesap kimliği

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
'SI

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint
Sertifika karması (Parmak Izi)

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
PSCredential nesnesini belirtir.
PSCredential nesnesi hakkında daha fazla bilgi için Get-Help Get-Credential yazın.

PSCredential nesnesi kuruluş KIMLIĞI kimlik bilgileri için Kullanıcı KIMLIĞI ve parola veya hizmet sorumlusu kimlik bilgileri için uygulama KIMLIĞI ve gizli 'yi sağlar.

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ortam
Oturum açacak hesabı içeren ortam

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal
Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Aboneliğin KIMLIĞINI belirtir.
Bu parametreyi belirtmezseniz, abonelik listesinin ilk aboneliği kullanılır.

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SubscriptionName
Abonelik adı

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Tenantıd
İsteğe bağlı kiracı adı veya KIMLIĞI

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### PSAzureProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

