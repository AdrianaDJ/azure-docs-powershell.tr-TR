---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592734"
---
# <span data-ttu-id="2ea6f-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ea6f-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2ea6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea6f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea6f-103">Geçici bir ağ erişimi isteği başlatır.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ea6f-104">SYNTAX</span></span>

### <span data-ttu-id="2ea6f-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ea6f-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea6f-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2ea6f-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ea6f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ea6f-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ea6f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ea6f-108">DESCRIPTION</span></span>
<span data-ttu-id="2ea6f-109">Geçici bir ağ erişimi isteği başlatır.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="2ea6f-110">İstek yapılandırılmış JıT ağ erişim ilkesiyle doğrulanır ve permittet, kullanıcının isteğine göre bir ağ bağlantısı açar.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="2ea6f-111">İstek daha sonra gözden geçirilmek üzere ilkede oturum açılır ve belirtilen süre aşıldığında sonlandırılır.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="2ea6f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ea6f-112">EXAMPLES</span></span>

### <span data-ttu-id="2ea6f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ea6f-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="2ea6f-114">Belirtilen bağlantı isteği verilerine göre bir ağ bağlantısı açar.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="2ea6f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ea6f-115">PARAMETERS</span></span>

### <span data-ttu-id="2ea6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea6f-116">-DefaultProfile</span></span>
<span data-ttu-id="2ea6f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea6f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ea6f-118">-InputObject</span></span>
<span data-ttu-id="2ea6f-119">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea6f-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="2ea6f-120">-Location</span></span>
<span data-ttu-id="2ea6f-121">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-121">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea6f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ea6f-122">-Name</span></span>
<span data-ttu-id="2ea6f-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ea6f-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea6f-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ea6f-126">-ResourceId</span></span>
<span data-ttu-id="2ea6f-127">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea6f-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2ea6f-128">-VirtualMachine</span></span>
<span data-ttu-id="2ea6f-129">Otomatik sağlama.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea6f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ea6f-130">-Confirm</span></span>
<span data-ttu-id="2ea6f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ea6f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea6f-132">-WhatIf</span></span>
<span data-ttu-id="2ea6f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ea6f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ea6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea6f-135">CommonParameters</span></span>
<span data-ttu-id="2ea6f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea6f-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea6f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea6f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ea6f-138">INPUTS</span></span>

### <span data-ttu-id="2ea6f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea6f-139">System.String</span></span>
<span data-ttu-id="2ea6f-140">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. Pssecuritymınnetworkaccesspolicyinitiatevirtualmachıne []</span><span class="sxs-lookup"><span data-stu-id="2ea6f-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="2ea6f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ea6f-141">OUTPUTS</span></span>

### <span data-ttu-id="2ea6f-142">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ea6f-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2ea6f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ea6f-143">NOTES</span></span>

## <span data-ttu-id="2ea6f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ea6f-144">RELATED LINKS</span></span>
