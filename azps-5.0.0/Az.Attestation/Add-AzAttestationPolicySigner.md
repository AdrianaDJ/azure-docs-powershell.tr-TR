---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322666"
---
# <span data-ttu-id="e1047-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="e1047-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="e1047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1047-102">SYNOPSIS</span></span>
<span data-ttu-id="e1047-103">Azure kanıt içinde kiracı için güvenilen bir ilke imzalayanı ekler.</span><span class="sxs-lookup"><span data-stu-id="e1047-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="e1047-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1047-104">SYNTAX</span></span>

### <span data-ttu-id="e1047-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1047-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1047-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e1047-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1047-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1047-107">DESCRIPTION</span></span>
<span data-ttu-id="e1047-108">Add-AzAttestationPolicySigner cmdlet 'i Azure kanıtlama 'ndaki bir kiracı için güvenilen bir ilke imzalayıcısı ekler.</span><span class="sxs-lookup"><span data-stu-id="e1047-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="e1047-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1047-109">EXAMPLES</span></span>

### <span data-ttu-id="e1047-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e1047-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="e1047-111">*Pshtest* adlı Atteestation sağlayıcısı için güvenilen bir imzalayan ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e1047-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="e1047-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1047-112">PARAMETERS</span></span>

### <span data-ttu-id="e1047-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1047-113">-DefaultProfile</span></span>
<span data-ttu-id="e1047-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1047-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1047-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1047-115">-Name</span></span>
<span data-ttu-id="e1047-116">Kanıt sağlayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1047-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="e1047-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1047-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1047-118">Bir kanıt sağlayıcısının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1047-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="e1047-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e1047-119">-ResourceId</span></span>
<span data-ttu-id="e1047-120">Bir kanıt sağlayıcısının RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1047-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="e1047-121">-İmzalayan</span><span class="sxs-lookup"><span data-stu-id="e1047-121">-Signer</span></span>
<span data-ttu-id="e1047-122">Değeri, "Maa-policyCertificate" adlı bir talep içeren, "-policyCertificate" adlı bir talep içeren,</span><span class="sxs-lookup"><span data-stu-id="e1047-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="e1047-123">RFC7519 JWT, mevcut güvenilen imzalama anahtarlarından biriyle imzalanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e1047-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="e1047-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1047-124">-Confirm</span></span>
<span data-ttu-id="e1047-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1047-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1047-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1047-126">-WhatIf</span></span>
<span data-ttu-id="e1047-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1047-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1047-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1047-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1047-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1047-129">CommonParameters</span></span>
<span data-ttu-id="e1047-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1047-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1047-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e1047-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1047-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1047-132">INPUTS</span></span>

### <span data-ttu-id="e1047-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e1047-133">System.String</span></span>

## <span data-ttu-id="e1047-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1047-134">OUTPUTS</span></span>

### <span data-ttu-id="e1047-135">Microsoft. Azure. Commands. kanıt. model. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="e1047-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="e1047-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1047-136">NOTES</span></span>

## <span data-ttu-id="e1047-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1047-137">RELATED LINKS</span></span>
