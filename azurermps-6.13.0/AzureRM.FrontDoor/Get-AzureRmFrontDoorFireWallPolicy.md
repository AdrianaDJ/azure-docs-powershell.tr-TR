---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591953"
---
# <span data-ttu-id="76303-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="76303-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="76303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76303-102">SYNOPSIS</span></span>
<span data-ttu-id="76303-103">WAF ilkesini alın</span><span class="sxs-lookup"><span data-stu-id="76303-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76303-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76303-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76303-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76303-105">DESCRIPTION</span></span>
<span data-ttu-id="76303-106">**Get-AzureRmFrontDoorFireWallPolicy** cmdletGet, geçerli aboneliğin altındaki bir kaynak grubundaki WAF ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="76303-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="76303-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76303-107">EXAMPLES</span></span>

### <span data-ttu-id="76303-108">Örnek 1: $resourceGroup $Name</span><span class="sxs-lookup"><span data-stu-id="76303-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="76303-109">$resourceGroup $Name adındaki bir WAF ilkesi alın</span><span class="sxs-lookup"><span data-stu-id="76303-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="76303-110">Örnek 2: $resourceGroup tüm WAF ilkesini alın</span><span class="sxs-lookup"><span data-stu-id="76303-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="76303-111">$resourceGroup 'de tüm WAF ilkesini alın</span><span class="sxs-lookup"><span data-stu-id="76303-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="76303-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76303-112">PARAMETERS</span></span>

### <span data-ttu-id="76303-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76303-113">-DefaultProfile</span></span>
<span data-ttu-id="76303-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76303-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76303-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="76303-115">-Name</span></span>
<span data-ttu-id="76303-116">FireWallPolicy adı.</span><span class="sxs-lookup"><span data-stu-id="76303-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="76303-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76303-117">-ResourceGroupName</span></span>
<span data-ttu-id="76303-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="76303-118">The resource group name.</span></span>

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

### <span data-ttu-id="76303-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76303-119">CommonParameters</span></span>
<span data-ttu-id="76303-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76303-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76303-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76303-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76303-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76303-122">INPUTS</span></span>

### <span data-ttu-id="76303-123">System. String</span><span class="sxs-lookup"><span data-stu-id="76303-123">System.String</span></span>

## <span data-ttu-id="76303-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76303-124">OUTPUTS</span></span>

### <span data-ttu-id="76303-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="76303-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="76303-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76303-126">NOTES</span></span>

## <span data-ttu-id="76303-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76303-127">RELATED LINKS</span></span>

<span data-ttu-id="76303-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="76303-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
