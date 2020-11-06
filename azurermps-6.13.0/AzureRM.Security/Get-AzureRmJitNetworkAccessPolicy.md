---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: bd366b636a29a08bea9124b3c3f4b9b423dc4deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587168"
---
# <span data-ttu-id="a8855-101">Get-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a8855-101">Get-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a8855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8855-102">SYNOPSIS</span></span>
<span data-ttu-id="a8855-103">JıT ağ erişim ilkelerini alır</span><span class="sxs-lookup"><span data-stu-id="a8855-103">Gets the JIT network access policies</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8855-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8855-104">SYNTAX</span></span>

### <span data-ttu-id="a8855-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a8855-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8855-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="a8855-106">ResourceGroupScope</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8855-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="a8855-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8855-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a8855-108">ResourceId</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8855-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8855-109">DESCRIPTION</span></span>
<span data-ttu-id="a8855-110">Tam zamanında (JıT) ağ erişimi ilkeleri, basit kullanıcıların bir VM 'ye geçici ağ bağlantısı oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a8855-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="a8855-111">İlke, bağlantı otomatik olarak kapatılmadan önce hangi bağlantı noktalarının, protokol ve kaynak IP adreslerinin bir VM bağlantısını ve en fazla süreyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a8855-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="a8855-112">İlkede, bu ilkeyle yapılan bağlantı isteğini de görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8855-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="a8855-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8855-113">EXAMPLES</span></span>

### <span data-ttu-id="a8855-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8855-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="a8855-115">Bir abonelikteki tüm JıT ağ erişim ilkeleri 'ni alma</span><span class="sxs-lookup"><span data-stu-id="a8855-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="a8855-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a8855-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="a8855-117">"MyService1" kaynak grubundaki tüm JıT ağ erişim ilkeleri 'ni alma</span><span class="sxs-lookup"><span data-stu-id="a8855-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="a8855-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a8855-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="a8855-119">Belirli bir JıT ağ erişim ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="a8855-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="a8855-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8855-120">PARAMETERS</span></span>

### <span data-ttu-id="a8855-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8855-121">-DefaultProfile</span></span>
<span data-ttu-id="a8855-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8855-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8855-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="a8855-123">-Location</span></span>
<span data-ttu-id="a8855-124">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="a8855-124">Location.</span></span>

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

### <span data-ttu-id="a8855-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8855-125">-Name</span></span>
<span data-ttu-id="a8855-126">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a8855-126">Resource name.</span></span>

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

### <span data-ttu-id="a8855-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8855-127">-ResourceGroupName</span></span>
<span data-ttu-id="a8855-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a8855-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8855-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a8855-129">-ResourceId</span></span>
<span data-ttu-id="a8855-130">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a8855-130">Resource ID.</span></span>

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

### <span data-ttu-id="a8855-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8855-131">CommonParameters</span></span>
<span data-ttu-id="a8855-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8855-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8855-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8855-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8855-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8855-134">INPUTS</span></span>

### <span data-ttu-id="a8855-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a8855-135">System.String</span></span>

## <span data-ttu-id="a8855-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8855-136">OUTPUTS</span></span>

### <span data-ttu-id="a8855-137">Microsoft. Azure. Commands. Security. modeller. Jnetworkaccesspolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a8855-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a8855-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8855-138">NOTES</span></span>

## <span data-ttu-id="a8855-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8855-139">RELATED LINKS</span></span>
