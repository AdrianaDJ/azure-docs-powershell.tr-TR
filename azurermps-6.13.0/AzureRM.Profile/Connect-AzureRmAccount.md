---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764601"
---
# Connect-AzureRmAccount

## SYNOPSIS
Azure Resource Manager cmdlet istekleriyle kullanmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanın.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Userwithsubscriptionıd (varsayılan)
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Serviceprincipalwithsubscriptionıd
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Serviceprincipalcertificatewithsubscriptionıd
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Accesstokenwithsubscriptionıd
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
Connect-AzureRmAccount cmdlet 'i Azure Resource Manager cmdlet istekleriyle kullanılmak üzere kimliği doğrulanmış bir hesapla Azure 'a bağlanır.
Bu kimliği doğrulanmış hesabı yalnızca Azure Resource Manager cmdlet 'leriyle kullanabilirsiniz.
Hizmet yönetimi cmdlet 'leriyle kullanılmak üzere kimliği doğrulanmış bir hesap eklemek için Add-AzureAccount veya Import-AzurePublishSettingsFile cmdlet 'ini kullanın.
Geçerli Kullanıcı için herhangi bir içerik bulunmazsa, bu komut kullanıcının bağlam listesini (ilk 25) aboneliklerinin her biri için bir içerikle doldurur. Kullanıcı için oluşturulan bağlamlar listesi, "Get-AzureRmContext-ListAvailable" çalıştırılarak bulunabilir. Bu bağlam popülasyonu atlamak için, bu komutu "-Skipcontextpopülasyonu" anahtar parametresiyle çalıştırabilirsiniz.
Bu cmdlet 'i çalıştırdıktan sonra, bağlantısı kesildi-AzureRmAccount kullanarak bir Azure hesabından bağlantınızı kesebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: Azure hesabına bağlanmak için etkileşimli oturum açma
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Bu komut bir Azure hesabına bağlanır.
Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için, istemde, Microsoft hesabı veya kuruluş KIMLIĞI kimlik bilgilerini sağlamanız gerekir.
Kimlik bilgileriniz için Multi-Factor Authentication etkinleştirilmişse, etkileşimli seçeneğini kullanarak oturum açmalı veya hizmet sorumlusu kimlik doğrulamasını kullanmalısınız.

### Örnek 2: kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure hesabına bağlanma
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

İlk komut Kullanıcı kimlik bilgilerini (Kullanıcı adı ve parola) sorar ve sonra bunları $Credential değişkeninde depolar.
İkinci komut $Credential depolanan kimlik bilgilerini kullanarak bir Azure hesabına bağlanır.
Bu hesap, kuruluş KIMLIĞI kimlik bilgilerini kullanarak Azure Resource Manager ile kimlik bilgilerini doğrular.
Azure Resource Manager cmdlet 'lerini bu hesapla çalıştırmak için Multi-Factor Authentication veya Microsoft hesabı kimlik bilgilerini kullanamazsınız.

### Örnek 3: Azure hizmet sorumlusu hesabına bağlanma
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

İlk komut, hizmet sorumlusu kimlik bilgilerini (uygulama kimliği ve hizmet sorumlusu parolası) alır ve bunları $Credential değişkeninde depolar.
İkinci komut, belirtilen kiracı için $Credential depolanan hizmet sorumlusu kimlik bilgilerini kullanarak Azure 'a bağlanır.
ServicePrincipal Switch parametresi hesabın hizmet sorumlusu olarak kimlik doğrulamasını gösterir.

### Örnek 4: belirli bir kiracı ve aboneliğe yönelik bir hesaba bağlanmak için etkileşimli oturum açma
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Bu komut bir Azure hesabına bağlanır ve varsayılan olarak belirtilen kiracı ve abonelik cmdlet 'lerini çalıştırmak için AzureRM PowerShell 'i çalıştırır.

### Örnek 5: yönetilen hizmet kimliği oturum kimliğini kullanarak hesap ekleme
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

Bu komut, ana bilgisayar ortamının yönetilen hizmet kimliğini kullanarak bağlanır (örneğin, atanmış yönetilen hizmet kimliğine sahip bir Virtuveren hizmeti

### Örnek 6: sertifikaları kullanarak hesap ekleme
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

Bu komut, sertifika tabanlı hizmet sorumlusu kimlik doğrulamasını kullanarak bir Azure hesabına bağlanır. Kimlik doğrulaması için kullanılan hizmet sorumlusu, verilen sertifikayla oluşturulmuş olmalıdır.

## PARAMETRELERINE

### -AccessToken
Bir erişim belirteci belirtir.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
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
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
'SI

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
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
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContextName
Bu oturumun varsayılan bağlamının adı.  Oturum açtıktan sonra bu bağlamı seçebilirsiniz.

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

### -Credential
PSCredential nesnesini belirtir.
PSCredential nesnesi hakkında daha fazla bilgi için Get-Help Get-Credential yazın.
PSCredential nesnesi kuruluş KIMLIĞI kimlik bilgileri için Kullanıcı KIMLIĞI ve parola veya hizmet sorumlusu kimlik bilgileri için uygulama KIMLIĞI ve gizli 'yi sağlar.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ortam
Oturum açacak hesabı içeren ortam

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Varsa, var olan içeriğin üzerine yazın.

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

### -GraphAccessToken
Grafik Hizmeti için AccessToken

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kimlik
Geçerli ortamdaki yönetilen hizmet kimliğini kullanarak oturum açın.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultAccessToken
Keykasa hizmeti için AccessToken

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Managedserviceanabilgisayaradı
Yönetilen hizmet oturumu ana bilgisayar adı

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServicePort
Yönetilen hizmet oturumu açma bağlantı noktası numarası

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceSecret
Gizli, yönetilen hizmet oturumu türleri için kullanılır.

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kapsam
Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal
Bu hesabın, hizmet sorumlusu kimlik bilgilerini sağlayarak doğruladığını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skipcontextpopülasyonu
İçerik oluşturmayı atlar.

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

### -SkipValidation
Erişim belirteci için doğrulamayı atlama

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonelik
Abonelik adı veya KIMLIĞI

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Tenantıd
İsteğe bağlı etki alanı adı veya kiracı KIMLIĞI. Tüm oturum açma durumlarında etki alanı adı çalışmaz. Bulut çözümü sağlayıcısı (CSP) oturum açma, kiracı KIMLIĞI gereklidir.

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String
Parametreler: abonelik (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
