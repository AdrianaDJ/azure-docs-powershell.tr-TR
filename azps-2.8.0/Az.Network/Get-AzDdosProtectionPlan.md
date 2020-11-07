---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 729f89742c7dd3249124f2d2404ab85f08db0e86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931777"
---
# <span data-ttu-id="fbc7b-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fbc7b-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="fbc7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc7b-103">Bir Vseçdos koruma planı alır.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="fbc7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbc7b-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbc7b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbc7b-105">DESCRIPTION</span></span>
<span data-ttu-id="fbc7b-106">Get-AzDdosProtectionPlan cmdlet 'i bir Vseçdos koruma planı alır.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="fbc7b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbc7b-107">EXAMPLES</span></span>

### <span data-ttu-id="fbc7b-108">Örnek 1: belirli bir Vseçdos koruma planı edinme</span><span class="sxs-lookup"><span data-stu-id="fbc7b-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="fbc7b-109">Bu durumda, sırasıyla, kaynak grubuna ve Vados koruma planının adına karşılık gelen hem **Resourcegroupname** hem de **Name** özniteliklerini belirtmemiz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="fbc7b-110">Örnek 2: kaynak grubundaki tüm Vseçdos koruma planlarını alma</span><span class="sxs-lookup"><span data-stu-id="fbc7b-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="fbc7b-111">Bu senaryoda, **Cıgrupgrupadi** parametresini yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="fbc7b-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="fbc7b-112">Örnek 3: abonelikteki tüm Vseçdos koruma planlarını alma</span><span class="sxs-lookup"><span data-stu-id="fbc7b-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="fbc7b-113">Burada, bir abonelikteki tüm Vseçdos koruma planlarının listesini almak için herhangi bir parametre belirtmiyoruz.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="fbc7b-114">Örnek 4: bir abonelikteki tüm Vseçdos koruma planlarını alma</span><span class="sxs-lookup"><span data-stu-id="fbc7b-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="fbc7b-115">Bu cmdlet, "test" ile başlayan tüm Vseçdosprotectionplanlar döndürür.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="fbc7b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbc7b-116">PARAMETERS</span></span>

### <span data-ttu-id="fbc7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc7b-117">-DefaultProfile</span></span>
<span data-ttu-id="fbc7b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbc7b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="fbc7b-119">-Name</span></span>
<span data-ttu-id="fbc7b-120">Vseçdos koruma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fbc7b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc7b-121">-ResourceGroupName</span></span>
<span data-ttu-id="fbc7b-122">Vseçdos koruma planı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fbc7b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc7b-123">CommonParameters</span></span>
<span data-ttu-id="fbc7b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc7b-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fbc7b-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc7b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbc7b-126">INPUTS</span></span>

### <span data-ttu-id="fbc7b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="fbc7b-127">System.String</span></span>

## <span data-ttu-id="fbc7b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbc7b-128">OUTPUTS</span></span>

### <span data-ttu-id="fbc7b-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fbc7b-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="fbc7b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbc7b-130">NOTES</span></span>

## <span data-ttu-id="fbc7b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbc7b-131">RELATED LINKS</span></span>

[<span data-ttu-id="fbc7b-132">Yeni-Azvadosprotectionplan</span><span class="sxs-lookup"><span data-stu-id="fbc7b-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="fbc7b-133">Remove-Azvseçdosprotectionplan</span><span class="sxs-lookup"><span data-stu-id="fbc7b-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="fbc7b-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fbc7b-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="fbc7b-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fbc7b-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="fbc7b-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fbc7b-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)