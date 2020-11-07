---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: 15b3e3fd90a7bacf87062bc12269ca2853276370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594583"
---
# <span data-ttu-id="b913d-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b913d-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="b913d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b913d-102">SYNOPSIS</span></span>
<span data-ttu-id="b913d-103">Var olan bir uygulamaya kimlik bilgisi ekler.</span><span class="sxs-lookup"><span data-stu-id="b913d-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b913d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b913d-104">SYNTAX</span></span>

### <span data-ttu-id="b913d-105">Applicationobjectivseçwithpasswordparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b913d-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b913d-106">Applicationobjectivseçwithcertvalueparameterset</span><span class="sxs-lookup"><span data-stu-id="b913d-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b913d-107">Applicationıdwithcertvalueparameterset</span><span class="sxs-lookup"><span data-stu-id="b913d-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b913d-108">Applicationıdwithpasswordparameterset</span><span class="sxs-lookup"><span data-stu-id="b913d-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b913d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b913d-109">DESCRIPTION</span></span>
<span data-ttu-id="b913d-110">New-AzureRmADAppCredential cmdlet 'i, bir uygulamanın yeni kimlik bilgilerini almak veya kimlik bilgilerini almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b913d-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="b913d-111">Uygulama, uygulama nesnesi kimliği veya uygulama kimliği sağlayarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="b913d-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="b913d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b913d-112">EXAMPLES</span></span>

### <span data-ttu-id="b913d-113">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b913d-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password P@ssw0rd!
```

<span data-ttu-id="b913d-114">Var olan bir uygulamaya yeni bir parola kimlik bilgisi eklenir.</span><span class="sxs-lookup"><span data-stu-id="b913d-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="b913d-115">Bu örnekte, sağlanan parola değeri uygulama nesnesi kimliği kullanılarak uygulamaya eklenir.</span><span class="sxs-lookup"><span data-stu-id="b913d-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="b913d-116">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b913d-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="b913d-117">Var olan bir uygulamaya yeni bir anahtar kimlik bilgisi eklenir.</span><span class="sxs-lookup"><span data-stu-id="b913d-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="b913d-118">Bu örnekte, sağlanan base64 kodlu genel x509 sertifikası ("MyApp. cer") ApplicationId kullanılarak uygulamaya eklenir.</span><span class="sxs-lookup"><span data-stu-id="b913d-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="b913d-119">--------------------------Örnek 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="b913d-119">--------------------------  Example 3  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="b913d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b913d-120">PARAMETERS</span></span>

### <span data-ttu-id="b913d-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b913d-121">-ApplicationId</span></span>
<span data-ttu-id="b913d-122">Kimlik bilgilerinin ekleneceği uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="b913d-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b913d-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b913d-123">-CertValue</span></span>
<span data-ttu-id="b913d-124">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="b913d-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b913d-125">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b913d-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b913d-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b913d-126">-EndDate</span></span>
<span data-ttu-id="b913d-127">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="b913d-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b913d-128">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="b913d-128">The default end date value is one year from today.</span></span> <span data-ttu-id="b913d-129">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b913d-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="b913d-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="b913d-130">-ObjectId</span></span>
<span data-ttu-id="b913d-131">Kimlik bilgilerinin ekleneceği uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="b913d-131">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b913d-132">-Parola</span><span class="sxs-lookup"><span data-stu-id="b913d-132">-Password</span></span>
<span data-ttu-id="b913d-133">Uygulamayla ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="b913d-133">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b913d-134">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b913d-134">-StartDate</span></span>
<span data-ttu-id="b913d-135">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="b913d-135">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b913d-136">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="b913d-136">The default start date value is today.</span></span>
<span data-ttu-id="b913d-137">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b913d-137">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="b913d-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="b913d-138">-Confirm</span></span>
<span data-ttu-id="b913d-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b913d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b913d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b913d-140">-WhatIf</span></span>
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

### <span data-ttu-id="b913d-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b913d-141">-DefaultProfile</span></span>
<span data-ttu-id="b913d-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b913d-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b913d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b913d-143">CommonParameters</span></span>
<span data-ttu-id="b913d-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b913d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b913d-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b913d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b913d-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b913d-146">INPUTS</span></span>

## <span data-ttu-id="b913d-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b913d-147">OUTPUTS</span></span>

### <span data-ttu-id="b913d-148">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="b913d-148">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="b913d-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b913d-149">NOTES</span></span>

## <span data-ttu-id="b913d-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b913d-150">RELATED LINKS</span></span>

[<span data-ttu-id="b913d-151">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b913d-151">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="b913d-152">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b913d-152">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="b913d-153">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b913d-153">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
