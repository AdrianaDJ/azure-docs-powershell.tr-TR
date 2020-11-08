---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b992f3a41278ba66c54eeefc0b548eef76b50980
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266349"
---
# <span data-ttu-id="b4e62-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4e62-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b4e62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e62-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e62-103">Geçici bir ağ erişimi isteği başlatır.</span><span class="sxs-lookup"><span data-stu-id="b4e62-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="b4e62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4e62-104">SYNTAX</span></span>

### <span data-ttu-id="b4e62-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4e62-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e62-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b4e62-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e62-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4e62-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e62-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4e62-108">DESCRIPTION</span></span>
<span data-ttu-id="b4e62-109">Geçici bir ağ erişimi isteği başlatır.</span><span class="sxs-lookup"><span data-stu-id="b4e62-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="b4e62-110">İstek, yapılandırılmış JıT ağ erişim ilkesiyle doğrulanır ve izin verildiğinde kullanıcının isteğine göre bir ağ bağlantısı açar.</span><span class="sxs-lookup"><span data-stu-id="b4e62-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="b4e62-111">İstek daha sonra gözden geçirilmek üzere ilkeye kaydedilir ve belirtilen süre aşıldığında sonlandırılır.</span><span class="sxs-lookup"><span data-stu-id="b4e62-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="b4e62-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4e62-112">EXAMPLES</span></span>

### <span data-ttu-id="b4e62-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4e62-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="b4e62-114">Belirtilen bağlantı isteği verilerine göre bir ağ bağlantısı açar.</span><span class="sxs-lookup"><span data-stu-id="b4e62-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="b4e62-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4e62-115">PARAMETERS</span></span>

### <span data-ttu-id="b4e62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e62-116">-DefaultProfile</span></span>
<span data-ttu-id="b4e62-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4e62-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4e62-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4e62-118">-InputObject</span></span>
<span data-ttu-id="b4e62-119">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b4e62-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e62-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="b4e62-120">-Location</span></span>
<span data-ttu-id="b4e62-121">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="b4e62-121">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e62-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4e62-122">-Name</span></span>
<span data-ttu-id="b4e62-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b4e62-123">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e62-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e62-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4e62-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4e62-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e62-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4e62-126">-ResourceId</span></span>
<span data-ttu-id="b4e62-127">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b4e62-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e62-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b4e62-128">-VirtualMachine</span></span>
<span data-ttu-id="b4e62-129">Otomatik sağlama.</span><span class="sxs-lookup"><span data-stu-id="b4e62-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e62-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4e62-130">-Confirm</span></span>
<span data-ttu-id="b4e62-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4e62-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e62-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e62-132">-WhatIf</span></span>
<span data-ttu-id="b4e62-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4e62-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4e62-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4e62-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4e62-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e62-135">CommonParameters</span></span>
<span data-ttu-id="b4e62-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4e62-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e62-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4e62-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e62-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4e62-138">INPUTS</span></span>

### <span data-ttu-id="b4e62-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4e62-139">System.String</span></span>

### <span data-ttu-id="b4e62-140">Microsoft. Azure. Commands. Security. cmdlet. Minetworkaccesspolicies. Pssecurityminetworkaccesspolicyinitiateinputobject</span><span class="sxs-lookup"><span data-stu-id="b4e62-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="b4e62-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4e62-141">OUTPUTS</span></span>

### <span data-ttu-id="b4e62-142">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4e62-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="b4e62-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4e62-143">NOTES</span></span>

## <span data-ttu-id="b4e62-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4e62-144">RELATED LINKS</span></span>
