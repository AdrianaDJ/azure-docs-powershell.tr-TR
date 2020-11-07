---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: ddb9bc19e852ae482dbbf687966c5f73f0a0a1d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759233"
---
# <span data-ttu-id="e730a-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e730a-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e730a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e730a-102">SYNOPSIS</span></span>
<span data-ttu-id="e730a-103">JıT Network Access ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e730a-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e730a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e730a-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e730a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e730a-105">DESCRIPTION</span></span>
<span data-ttu-id="e730a-106">JıT Network Access ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e730a-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e730a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e730a-107">EXAMPLES</span></span>

### <span data-ttu-id="e730a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e730a-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="e730a-109">Yeni VM kurallarıyla JıT ağ erişimi ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e730a-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="e730a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e730a-110">PARAMETERS</span></span>

### <span data-ttu-id="e730a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e730a-111">-DefaultProfile</span></span>
<span data-ttu-id="e730a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e730a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e730a-113">-Tür</span><span class="sxs-lookup"><span data-stu-id="e730a-113">-Kind</span></span>
<span data-ttu-id="e730a-114">Türünde.</span><span class="sxs-lookup"><span data-stu-id="e730a-114">Kind.</span></span>

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

### <span data-ttu-id="e730a-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="e730a-115">-Location</span></span>
<span data-ttu-id="e730a-116">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="e730a-116">Location.</span></span>

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

### <span data-ttu-id="e730a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e730a-117">-Name</span></span>
<span data-ttu-id="e730a-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="e730a-118">Resource name.</span></span>

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

### <span data-ttu-id="e730a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e730a-119">-ResourceGroupName</span></span>
<span data-ttu-id="e730a-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e730a-120">Resource group name.</span></span>

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

### <span data-ttu-id="e730a-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e730a-121">-VirtualMachine</span></span>
<span data-ttu-id="e730a-122">Virutal makineleri.</span><span class="sxs-lookup"><span data-stu-id="e730a-122">Virutal Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e730a-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e730a-123">-Confirm</span></span>
<span data-ttu-id="e730a-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e730a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e730a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e730a-125">-WhatIf</span></span>
<span data-ttu-id="e730a-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e730a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e730a-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e730a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e730a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e730a-128">CommonParameters</span></span>
<span data-ttu-id="e730a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e730a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e730a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e730a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e730a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e730a-131">INPUTS</span></span>

### <span data-ttu-id="e730a-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e730a-132">None</span></span>

## <span data-ttu-id="e730a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e730a-133">OUTPUTS</span></span>

### <span data-ttu-id="e730a-134">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e730a-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e730a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e730a-135">NOTES</span></span>

## <span data-ttu-id="e730a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e730a-136">RELATED LINKS</span></span>
