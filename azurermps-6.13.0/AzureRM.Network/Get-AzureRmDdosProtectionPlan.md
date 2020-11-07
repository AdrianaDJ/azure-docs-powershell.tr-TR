---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763443"
---
# <span data-ttu-id="9fcc1-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fcc1-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="9fcc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="9fcc1-103">Bir Vseçdos koruma planı alır.</span><span class="sxs-lookup"><span data-stu-id="9fcc1-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fcc1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fcc1-104">SYNTAX</span></span>

### <span data-ttu-id="9fcc1-105">Grup</span><span class="sxs-lookup"><span data-stu-id="9fcc1-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fcc1-106">Listeniz</span><span class="sxs-lookup"><span data-stu-id="9fcc1-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fcc1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fcc1-107">DESCRIPTION</span></span>
<span data-ttu-id="9fcc1-108">Get-AzureRmDdosProtectionPlan cmdlet 'i bir Vseçdos koruma planı alır.</span><span class="sxs-lookup"><span data-stu-id="9fcc1-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="9fcc1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fcc1-109">EXAMPLES</span></span>

### <span data-ttu-id="9fcc1-110">Örnek 1: belirli bir Vseçdos koruma planı edinme</span><span class="sxs-lookup"><span data-stu-id="9fcc1-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


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

<span data-ttu-id="9fcc1-111">Bu durumda, sırasıyla, kaynak grubuna ve Vados koruma planının adına karşılık gelen hem **Resourcegroupname** hem de **Name** özniteliklerini belirtmemiz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9fcc1-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="9fcc1-112">Örnek 2: kaynak grubundaki tüm Vseçdos koruma planlarını alma</span><span class="sxs-lookup"><span data-stu-id="9fcc1-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


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

<span data-ttu-id="9fcc1-113">Bu senaryoda, **Cıgrupgrupadi** parametresini yalnızca bir</span><span class="sxs-lookup"><span data-stu-id="9fcc1-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="9fcc1-114">Örnek 2: bir abonelikteki tüm Vseçdos koruma planlarını alma</span><span class="sxs-lookup"><span data-stu-id="9fcc1-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


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

<span data-ttu-id="9fcc1-115">Burada, bir abonelikteki tüm Vseçdos koruma planlarının listesini almak için herhangi bir parametre belirtmiyoruz.</span><span class="sxs-lookup"><span data-stu-id="9fcc1-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="9fcc1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fcc1-116">PARAMETERS</span></span>

### <span data-ttu-id="9fcc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fcc1-117">-DefaultProfile</span></span>
<span data-ttu-id="9fcc1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9fcc1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fcc1-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9fcc1-119">-Name</span></span>
<span data-ttu-id="9fcc1-120">Vseçdos koruma planının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fcc1-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fcc1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fcc1-121">-ResourceGroupName</span></span>
<span data-ttu-id="9fcc1-122">Vseçdos koruma planı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fcc1-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fcc1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fcc1-123">CommonParameters</span></span>
<span data-ttu-id="9fcc1-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fcc1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fcc1-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fcc1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fcc1-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fcc1-126">INPUTS</span></span>

### <span data-ttu-id="9fcc1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9fcc1-127">System.String</span></span>

## <span data-ttu-id="9fcc1-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fcc1-128">OUTPUTS</span></span>

### <span data-ttu-id="9fcc1-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fcc1-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="9fcc1-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fcc1-130">NOTES</span></span>

## <span data-ttu-id="9fcc1-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fcc1-131">RELATED LINKS</span></span>

[<span data-ttu-id="9fcc1-132">Yeni-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fcc1-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="9fcc1-133">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="9fcc1-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="9fcc1-134">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fcc1-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9fcc1-135">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fcc1-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9fcc1-136">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fcc1-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
