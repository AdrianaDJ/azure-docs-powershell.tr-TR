---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589341"
---
# <span data-ttu-id="1a7f5-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a7f5-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="1a7f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="1a7f5-103">JıT Network Access ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a7f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a7f5-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a7f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a7f5-105">DESCRIPTION</span></span>
<span data-ttu-id="1a7f5-106">JıT Network Access ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="1a7f5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a7f5-107">EXAMPLES</span></span>

### <span data-ttu-id="1a7f5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1a7f5-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="1a7f5-109">Yeni VM kurallarıyla JıT ağ erişimi ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="1a7f5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a7f5-110">PARAMETERS</span></span>

### <span data-ttu-id="1a7f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a7f5-111">-DefaultProfile</span></span>
<span data-ttu-id="1a7f5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a7f5-113">-Tür</span><span class="sxs-lookup"><span data-stu-id="1a7f5-113">-Kind</span></span>
<span data-ttu-id="1a7f5-114">Türünde.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7f5-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="1a7f5-115">-Location</span></span>
<span data-ttu-id="1a7f5-116">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7f5-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a7f5-117">-Name</span></span>
<span data-ttu-id="1a7f5-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7f5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a7f5-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a7f5-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7f5-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1a7f5-121">-VirtualMachine</span></span>
<span data-ttu-id="1a7f5-122">Virutal makineleri.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7f5-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a7f5-123">-Confirm</span></span>
<span data-ttu-id="1a7f5-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a7f5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a7f5-125">-WhatIf</span></span>
<span data-ttu-id="1a7f5-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a7f5-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a7f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a7f5-128">CommonParameters</span></span>
<span data-ttu-id="1a7f5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a7f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a7f5-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a7f5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a7f5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a7f5-131">INPUTS</span></span>

### <span data-ttu-id="1a7f5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a7f5-132">System.String</span></span>
<span data-ttu-id="1a7f5-133">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. Pssecuritymınnetworkaccesspolicyvirtualmachine []</span><span class="sxs-lookup"><span data-stu-id="1a7f5-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="1a7f5-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a7f5-134">OUTPUTS</span></span>

### <span data-ttu-id="1a7f5-135">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a7f5-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="1a7f5-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a7f5-136">NOTES</span></span>

## <span data-ttu-id="1a7f5-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a7f5-137">RELATED LINKS</span></span>
