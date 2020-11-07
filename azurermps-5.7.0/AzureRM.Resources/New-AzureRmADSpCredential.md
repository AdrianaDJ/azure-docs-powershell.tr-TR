---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591628"
---
# <span data-ttu-id="3d592-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3d592-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="3d592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d592-102">SYNOPSIS</span></span>
<span data-ttu-id="3d592-103">Var olan hizmet sorumlusuna kimlik bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="3d592-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d592-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d592-104">SYNTAX</span></span>

### <span data-ttu-id="3d592-105">Spobjectivseçwithpasswordparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d592-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d592-106">Spobjectivseçwithcertvalueparameterset</span><span class="sxs-lookup"><span data-stu-id="3d592-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d592-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d592-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d592-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d592-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d592-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d592-109">DESCRIPTION</span></span>
<span data-ttu-id="3d592-110">New-AzureRmADSpCredential cmdlet 'i, yeni kimlik bilgileri eklemek veya hizmet sorumlusu için kimlik bilgilerini almak üzere kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3d592-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="3d592-111">Hizmet sorumlusu, nesne kimliği veya hizmet asıl adı vererek tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="3d592-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="3d592-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d592-112">EXAMPLES</span></span>

### <span data-ttu-id="3d592-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3d592-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

<span data-ttu-id="3d592-114">Var olan hizmet sorumlusuna yeni bir parola kimlik bilgisi eklenir.</span><span class="sxs-lookup"><span data-stu-id="3d592-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="3d592-115">Bu örnekte, sağlanan parola değeri ObjectID kullanılarak hizmet sorumlusuna eklenir.</span><span class="sxs-lookup"><span data-stu-id="3d592-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="3d592-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3d592-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="3d592-117">Var olan hizmet sorumlusuna yeni bir anahtar kimlik bilgisi eklenir.</span><span class="sxs-lookup"><span data-stu-id="3d592-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="3d592-118">Bu örnekte, sağlanan base64 kodlu genel x509 sertifikası ("MyApp. cer") SPN 'yi kullanarak hizmet sorumlusuna eklenir.</span><span class="sxs-lookup"><span data-stu-id="3d592-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="3d592-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3d592-119">Example 3</span></span>

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="3d592-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d592-120">PARAMETERS</span></span>

### <span data-ttu-id="3d592-121">-CertValue</span><span class="sxs-lookup"><span data-stu-id="3d592-121">-CertValue</span></span>
<span data-ttu-id="3d592-122">"Asimetrik" kimlik bilgileri türü.</span><span class="sxs-lookup"><span data-stu-id="3d592-122">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="3d592-123">Temel 64 kodlu sertifikayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3d592-123">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d592-124">-DefaultProfile</span></span>
<span data-ttu-id="3d592-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3d592-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="3d592-126">-EndDate</span></span>
<span data-ttu-id="3d592-127">Kimlik bilgisi kullanımının geçerli bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="3d592-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="3d592-128">Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="3d592-128">The default end date value is one year from today.</span></span> <span data-ttu-id="3d592-129">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3d592-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="3d592-130">-ObjectId</span></span>
<span data-ttu-id="3d592-131">Kimlik bilgilerini eklemek için hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="3d592-131">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-132">-Parola</span><span class="sxs-lookup"><span data-stu-id="3d592-132">-Password</span></span>
<span data-ttu-id="3d592-133">Uygulamayla ilişkilendirilecek parola.</span><span class="sxs-lookup"><span data-stu-id="3d592-133">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d592-134">-ServicePrincipalName</span></span>
<span data-ttu-id="3d592-135">Kimlik bilgilerinin ekleneceği hizmet sorumlusunun adı (SPN).</span><span class="sxs-lookup"><span data-stu-id="3d592-135">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="3d592-136">-StartDate</span></span>
<span data-ttu-id="3d592-137">Kimlik bilgisi kullanımının geçerli başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="3d592-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="3d592-138">Varsayılan başlangıç tarihi değeri bugün.</span><span class="sxs-lookup"><span data-stu-id="3d592-138">The default start date value is today.</span></span> <span data-ttu-id="3d592-139">"Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3d592-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d592-140">-Confirm</span></span>
<span data-ttu-id="3d592-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d592-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d592-142">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d592-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d592-143">CommonParameters</span></span>
<span data-ttu-id="3d592-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d592-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d592-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d592-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d592-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d592-146">INPUTS</span></span>

### <span data-ttu-id="3d592-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3d592-147">None</span></span>
<span data-ttu-id="3d592-148">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3d592-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d592-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d592-149">OUTPUTS</span></span>

### <span data-ttu-id="3d592-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="3d592-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="3d592-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d592-151">NOTES</span></span>

## <span data-ttu-id="3d592-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d592-152">RELATED LINKS</span></span>

[<span data-ttu-id="3d592-153">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3d592-153">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="3d592-154">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3d592-154">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="3d592-155">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3d592-155">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)


