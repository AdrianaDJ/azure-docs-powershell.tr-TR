---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: a0e4f0c877d43ffa49737e3c3a180783a385c795
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760498"
---
# <span data-ttu-id="46d24-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46d24-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="46d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46d24-102">SYNOPSIS</span></span>
<span data-ttu-id="46d24-103">Hizmet uç noktası İlkesi tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="46d24-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="46d24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46d24-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46d24-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46d24-105">DESCRIPTION</span></span>
<span data-ttu-id="46d24-106">**Get-AzServiceEndpointPolicyDefinition** cmdlet 'i bir hizmet uç noktası İlkesi tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="46d24-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="46d24-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46d24-107">EXAMPLES</span></span>

### <span data-ttu-id="46d24-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46d24-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="46d24-109">Bu komut, ServiceEndpointPolicy 'da ServiceEndpointPolicyDefinition1 adındaki hizmet uç noktası İlkesi tanımını alır $Policy $policydef değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="46d24-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="46d24-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46d24-110">PARAMETERS</span></span>

### <span data-ttu-id="46d24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d24-111">-DefaultProfile</span></span>
<span data-ttu-id="46d24-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46d24-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46d24-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="46d24-113">-Name</span></span>
<span data-ttu-id="46d24-114">Hizmet uç noktası ilke tanımının adı</span><span class="sxs-lookup"><span data-stu-id="46d24-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="46d24-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="46d24-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="46d24-116">Hizmet bitiş noktası İlkesi</span><span class="sxs-lookup"><span data-stu-id="46d24-116">The Service endpoint policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d24-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="46d24-117">-Confirm</span></span>
<span data-ttu-id="46d24-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46d24-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d24-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d24-119">-WhatIf</span></span>
<span data-ttu-id="46d24-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46d24-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46d24-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46d24-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d24-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d24-122">CommonParameters</span></span>
<span data-ttu-id="46d24-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46d24-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d24-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46d24-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d24-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46d24-125">INPUTS</span></span>

### <span data-ttu-id="46d24-126">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="46d24-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="46d24-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46d24-127">OUTPUTS</span></span>

### <span data-ttu-id="46d24-128">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46d24-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="46d24-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46d24-129">NOTES</span></span>

## <span data-ttu-id="46d24-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46d24-130">RELATED LINKS</span></span>

[<span data-ttu-id="46d24-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46d24-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="46d24-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46d24-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="46d24-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46d24-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="46d24-134">Set-Azhizmetiendpointpolicydefinition</span><span class="sxs-lookup"><span data-stu-id="46d24-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)