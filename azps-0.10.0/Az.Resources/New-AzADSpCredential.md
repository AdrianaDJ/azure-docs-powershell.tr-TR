---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 4c68470b97134019b0abf7724012f3a6fab4627f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936414"
---
# <span data-ttu-id="1a617-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1a617-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="1a617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a617-102">SYNOPSIS</span></span>
<span data-ttu-id="1a617-103">Var olan hizmet sorumlusuna kimlik bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="1a617-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="1a617-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a617-104">SYNTAX</span></span>

### <span data-ttu-id="1a617-105">Spobjectivseçwithpasswordparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a617-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a617-106">Spobjectivseçwithcertvalueparameterset</span><span class="sxs-lookup"><span data-stu-id="1a617-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a617-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a617-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a617-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a617-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a617-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a617-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a617-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a617-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a617-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a617-111">DESCRIPTION</span></span>
<span data-ttu-id="1a617-112">New-AzADSpCredential cmdlet 'i, yeni kimlik bilgileri eklemek veya hizmet sorumlusu için kimlik bilgilerini almak üzere kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1a617-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="1a617-113">Hizmet sorumlusu, nesne kimliği veya hizmet asıl adı vererek tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="1a617-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="1a617-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a617-114">EXAMPLES</span></span>

### <span data-ttu-id="1a617-115">Örnek 1-oluşturulan parola kullanarak yeni bir hizmet sorumlusu kimlik bilgisi oluşturur</span><span class="sxs-lookup"><span data-stu-id="1a617-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="1a617-116">' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' nesne kimliğine sahip mevcut hizmet sorumlusuna yeni bir parola kimlik bilgileri eklenir.</span><span class="sxs-lookup"><span data-stu-id="1a617-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="1a617-117">Örnek 2-sertifika kullanarak yeni bir hizmet sorumlusu kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a617-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="1a617-118">Sağlanan base64 kodlu genel x509 sertifikası ("MyApp. cer"), SPN 'YI kullanarak var olan hizmet sorumlusuna eklenir.</span><span class="sxs-lookup"><span data-stu-id="1a617-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="1a617-119">Örnek 3-boru kullanarak yeni bir hizmet sorumlusu kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a617-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="1a617-120">' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' ile hizmet sorumlusunu alır ve bu hizmet sorumlusu için oluşturulmuş parolayla yeni bir hizmet sorumlusu kimlik bilgisi oluşturmaya yönelik New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="1a617-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="1a617-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a617-121">PARAMETERS</span></span>

### <span data-ttu-id="1a617-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="1a617-122">-CertValue</span></span>
<span data-ttu-id="1a617-123">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="1a617-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="1a617-124">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1a617-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="1a617-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a617-125">-DefaultProfile</span></span>
<span data-ttu-id="1a617-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1a617-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a617-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="1a617-127">-EndDate</span></span>
<span data-ttu-id="1a617-128">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="1a617-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="1a617-129">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="1a617-129">The default end date value is one year from today.</span></span> <span data-ttu-id="1a617-130">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1a617-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="1a617-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="1a617-131">-ObjectId</span></span>
<span data-ttu-id="1a617-132">Kimlik bilgilerini eklemek için hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="1a617-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a617-133">-Parola</span><span class="sxs-lookup"><span data-stu-id="1a617-133">-Password</span></span>
<span data-ttu-id="1a617-134">Uygulamayla ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="1a617-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a617-135">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1a617-135">-ServicePrincipalName</span></span>
<span data-ttu-id="1a617-136">Kimlik bilgilerinin ekleneceği hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="1a617-136">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="1a617-137">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="1a617-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="1a617-138">Kimlik bilgilerinin ekleneceği hizmet sorumlusu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1a617-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a617-139">-StartDate</span><span class="sxs-lookup"><span data-stu-id="1a617-139">-StartDate</span></span>
<span data-ttu-id="1a617-140">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="1a617-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="1a617-141">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="1a617-141">The default start date value is today.</span></span> <span data-ttu-id="1a617-142">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1a617-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="1a617-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a617-143">-Confirm</span></span>
<span data-ttu-id="1a617-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a617-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a617-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a617-145">-WhatIf</span></span>
<span data-ttu-id="1a617-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a617-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a617-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a617-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a617-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a617-148">CommonParameters</span></span>
<span data-ttu-id="1a617-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a617-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a617-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a617-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a617-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a617-151">INPUTS</span></span>

### <span data-ttu-id="1a617-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="1a617-152">System.Guid</span></span>

### <span data-ttu-id="1a617-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1a617-153">System.String</span></span>

### <span data-ttu-id="1a617-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1a617-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="1a617-155">Parametreler: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1a617-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="1a617-156">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1a617-156">System.Security.SecureString</span></span>

### <span data-ttu-id="1a617-157">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="1a617-157">System.DateTime</span></span>

## <span data-ttu-id="1a617-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a617-158">OUTPUTS</span></span>

### <span data-ttu-id="1a617-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="1a617-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="1a617-160">Microsoft. Azure. Commands. resources. modeller. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="1a617-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="1a617-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a617-161">NOTES</span></span>

## <span data-ttu-id="1a617-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a617-162">RELATED LINKS</span></span>

[<span data-ttu-id="1a617-163">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1a617-163">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="1a617-164">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1a617-164">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="1a617-165">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1a617-165">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



