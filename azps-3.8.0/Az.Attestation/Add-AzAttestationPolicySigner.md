---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: df46bc097ce4a1a52c486bb0e418bce656f0f476
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098220"
---
# <span data-ttu-id="d9c41-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="d9c41-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="d9c41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c41-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c41-103">Azure kanıt içinde kiracı için güvenilen bir ilke imzalayanı ekler.</span><span class="sxs-lookup"><span data-stu-id="d9c41-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="d9c41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9c41-104">SYNTAX</span></span>

### <span data-ttu-id="d9c41-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9c41-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9c41-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d9c41-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c41-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9c41-107">DESCRIPTION</span></span>
<span data-ttu-id="d9c41-108">Add-AzAttestationPolicySigner cmdlet 'i Azure kanıtlama 'ndaki bir kiracı için güvenilen bir ilke imzalayıcısı ekler.</span><span class="sxs-lookup"><span data-stu-id="d9c41-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="d9c41-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9c41-109">EXAMPLES</span></span>

### <span data-ttu-id="d9c41-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d9c41-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="d9c41-111">*Pshtest* adlı Atteestation sağlayıcısı için güvenilen bir imzalayan ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d9c41-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="d9c41-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9c41-112">PARAMETERS</span></span>

### <span data-ttu-id="d9c41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c41-113">-DefaultProfile</span></span>
<span data-ttu-id="d9c41-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9c41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9c41-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9c41-115">-Name</span></span>
<span data-ttu-id="d9c41-116">Kanıt sağlayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9c41-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c41-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9c41-118">Bir kanıt sağlayıcısının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9c41-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c41-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d9c41-119">-ResourceId</span></span>
<span data-ttu-id="d9c41-120">Bir kanıt sağlayıcısının RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9c41-120">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c41-121">-İmzalayan</span><span class="sxs-lookup"><span data-stu-id="d9c41-121">-Signer</span></span>
<span data-ttu-id="d9c41-122">Değeri, "AAS-policyCertificate" adlı bir talep içeren bir talep içeren bir talep içeren RFC7519</span><span class="sxs-lookup"><span data-stu-id="d9c41-122">Specifies the RFC7519 JSON Web Token containing a claim named "aas-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="d9c41-123">RFC7519 JWT, mevcut güvenilen imzalama anahtarlarından biriyle imzalanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d9c41-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c41-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9c41-124">-Confirm</span></span>
<span data-ttu-id="d9c41-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9c41-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c41-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c41-126">-WhatIf</span></span>
<span data-ttu-id="d9c41-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9c41-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c41-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9c41-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c41-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c41-129">CommonParameters</span></span>
<span data-ttu-id="d9c41-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9c41-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c41-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d9c41-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c41-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9c41-132">INPUTS</span></span>

### <span data-ttu-id="d9c41-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d9c41-133">System.String</span></span>

## <span data-ttu-id="d9c41-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9c41-134">OUTPUTS</span></span>

### <span data-ttu-id="d9c41-135">Microsoft. Azure. Commands. kanıt. model. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="d9c41-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="d9c41-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9c41-136">NOTES</span></span>

## <span data-ttu-id="d9c41-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9c41-137">RELATED LINKS</span></span>
