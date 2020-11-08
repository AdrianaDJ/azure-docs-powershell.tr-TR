---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 46977fe6b2e6cf3c3811c7d9bbd49262b06cec54
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107663"
---
# <span data-ttu-id="038ab-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="038ab-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="038ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="038ab-102">SYNOPSIS</span></span>
<span data-ttu-id="038ab-103">Var olan hizmet sorumlusuna kimlik bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="038ab-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="038ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="038ab-104">SYNTAX</span></span>

### <span data-ttu-id="038ab-105">Spobjectivseçwithpasswordparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="038ab-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="038ab-106">Spobjectivseçwithcertvalueparameterset</span><span class="sxs-lookup"><span data-stu-id="038ab-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="038ab-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="038ab-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="038ab-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="038ab-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="038ab-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="038ab-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="038ab-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="038ab-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="038ab-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="038ab-111">DESCRIPTION</span></span>
<span data-ttu-id="038ab-112">New-AzADSpCredential cmdlet 'i, yeni kimlik bilgileri eklemek veya hizmet sorumlusu için kimlik bilgilerini almak üzere kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="038ab-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="038ab-113">Hizmet sorumlusu, nesne kimliği veya hizmet asıl adı vererek tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="038ab-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="038ab-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="038ab-114">EXAMPLES</span></span>

### <span data-ttu-id="038ab-115">Örnek 1: oluşturulmuş parola kullanarak yeni bir hizmet sorumlusu kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="038ab-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="038ab-116">' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' nesne kimliğine sahip mevcut hizmet sorumlusuna yeni bir parola kimlik bilgileri eklenir.</span><span class="sxs-lookup"><span data-stu-id="038ab-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="038ab-117">Örnek 2: sertifika kullanarak yeni bir hizmet sorumlusu kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="038ab-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="038ab-118">Sağlanan base64 kodlu genel x509 sertifikası ("MyApp. cer"), SPN 'YI kullanarak var olan hizmet sorumlusuna eklenir.</span><span class="sxs-lookup"><span data-stu-id="038ab-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="038ab-119">Örnek 3: boru kullanarak yeni bir hizmet sorumlusu kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="038ab-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="038ab-120">' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' ile hizmet sorumlusunu alır ve bu hizmet sorumlusu için oluşturulmuş parolayla yeni bir hizmet sorumlusu kimlik bilgisi oluşturmaya yönelik New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="038ab-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="038ab-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="038ab-121">PARAMETERS</span></span>

### <span data-ttu-id="038ab-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="038ab-122">-CertValue</span></span>
<span data-ttu-id="038ab-123">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="038ab-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="038ab-124">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="038ab-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="038ab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038ab-125">-DefaultProfile</span></span>
<span data-ttu-id="038ab-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="038ab-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="038ab-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="038ab-127">-EndDate</span></span>
<span data-ttu-id="038ab-128">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="038ab-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="038ab-129">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="038ab-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="038ab-130">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="038ab-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="038ab-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="038ab-131">-ObjectId</span></span>
<span data-ttu-id="038ab-132">Kimlik bilgilerini eklemek için hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="038ab-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="038ab-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="038ab-133">-ServicePrincipalName</span></span>
<span data-ttu-id="038ab-134">Kimlik bilgilerinin ekleneceği hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="038ab-134">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="038ab-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="038ab-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="038ab-136">Kimlik bilgilerinin ekleneceği hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="038ab-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="038ab-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="038ab-137">-StartDate</span></span>
<span data-ttu-id="038ab-138">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="038ab-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="038ab-139">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="038ab-139">The default start date value is today.</span></span>
<span data-ttu-id="038ab-140">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="038ab-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="038ab-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="038ab-141">-Confirm</span></span>
<span data-ttu-id="038ab-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="038ab-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="038ab-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="038ab-143">-WhatIf</span></span>
<span data-ttu-id="038ab-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="038ab-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="038ab-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="038ab-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="038ab-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038ab-146">CommonParameters</span></span>
<span data-ttu-id="038ab-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="038ab-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038ab-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="038ab-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038ab-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="038ab-149">INPUTS</span></span>

### <span data-ttu-id="038ab-150">System. String</span><span class="sxs-lookup"><span data-stu-id="038ab-150">System.String</span></span>

### <span data-ttu-id="038ab-151">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="038ab-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="038ab-152">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="038ab-152">System.DateTime</span></span>

## <span data-ttu-id="038ab-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="038ab-153">OUTPUTS</span></span>

### <span data-ttu-id="038ab-154">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="038ab-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="038ab-155">Microsoft. Azure. Commands. resources. modeller. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="038ab-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="038ab-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="038ab-156">NOTES</span></span>

## <span data-ttu-id="038ab-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="038ab-157">RELATED LINKS</span></span>

[<span data-ttu-id="038ab-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="038ab-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="038ab-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="038ab-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="038ab-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="038ab-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



