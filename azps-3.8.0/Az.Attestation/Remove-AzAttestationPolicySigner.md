---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: 8f06713ab61ca423fee031f8dca9df90b941ed32
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098214"
---
# <span data-ttu-id="05163-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="05163-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="05163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05163-102">SYNOPSIS</span></span>
<span data-ttu-id="05163-103">Azure kanıtlama 'ndaki bir kiracı için güvenilen ilke imzacısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="05163-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="05163-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05163-104">SYNTAX</span></span>

### <span data-ttu-id="05163-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="05163-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05163-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="05163-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05163-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="05163-107">DESCRIPTION</span></span>
<span data-ttu-id="05163-108">Remove-AzAttestationPolicySigner cmdlet 'i Azure kanıtlama 'ndaki bir kiracı için güvenilen ilke imzacısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="05163-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="05163-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05163-109">EXAMPLES</span></span>

### <span data-ttu-id="05163-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="05163-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="05163-111">*Pshtest* adındaki kanıtlama sağlayıcısı için güvenilen İmzalayanın kaldırma.</span><span class="sxs-lookup"><span data-stu-id="05163-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="05163-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05163-112">PARAMETERS</span></span>

### <span data-ttu-id="05163-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05163-113">-DefaultProfile</span></span>
<span data-ttu-id="05163-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05163-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05163-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="05163-115">-Name</span></span>
<span data-ttu-id="05163-116">Kanıt sağlayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05163-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="05163-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05163-117">-ResourceGroupName</span></span>
<span data-ttu-id="05163-118">Bir kanıt sağlayıcısının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05163-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="05163-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="05163-119">-ResourceId</span></span>
<span data-ttu-id="05163-120">Bir kanıt sağlayıcısının RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="05163-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="05163-121">-İmzalayan</span><span class="sxs-lookup"><span data-stu-id="05163-121">-Signer</span></span>
<span data-ttu-id="05163-122">Değeri, "AAS-policyCertificate" adlı bir talep içeren ve değeri, kaldırmak üzere güvenilir bir imzalama anahtarı içeren RFC7517 JSON Web anahtarı olan RFC7519 JSON Web belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05163-122">Specifies the RFC7519 JSON Web Token containing a claim named "aas-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="05163-123">RFC7519 JWT, mevcut güvenilen imzalama anahtarlarından biriyle imzalanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="05163-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="05163-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="05163-124">-Confirm</span></span>
<span data-ttu-id="05163-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05163-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05163-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05163-126">-WhatIf</span></span>
<span data-ttu-id="05163-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05163-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05163-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05163-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05163-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05163-129">CommonParameters</span></span>
<span data-ttu-id="05163-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05163-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05163-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="05163-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05163-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05163-132">INPUTS</span></span>

### <span data-ttu-id="05163-133">System. String</span><span class="sxs-lookup"><span data-stu-id="05163-133">System.String</span></span>

## <span data-ttu-id="05163-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05163-134">OUTPUTS</span></span>

### <span data-ttu-id="05163-135">Microsoft. Azure. Commands. kanıt. model. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="05163-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="05163-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05163-136">NOTES</span></span>

## <span data-ttu-id="05163-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05163-137">RELATED LINKS</span></span>
