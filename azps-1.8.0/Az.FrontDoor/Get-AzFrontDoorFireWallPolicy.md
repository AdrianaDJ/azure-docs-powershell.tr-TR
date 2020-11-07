---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: e8fe8fb59ee56e457c49d959c07db08cad62bb5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916768"
---
# <span data-ttu-id="dc089-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="dc089-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="dc089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc089-102">SYNOPSIS</span></span>
<span data-ttu-id="dc089-103">WAF ilkesini alın</span><span class="sxs-lookup"><span data-stu-id="dc089-103">Get WAF policy</span></span>

## <span data-ttu-id="dc089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc089-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc089-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc089-105">DESCRIPTION</span></span>
<span data-ttu-id="dc089-106">**Get-AzFrontDoorFireWallPolicy** cmdletGet, geçerli aboneliğin altındaki bir kaynak grubundaki WAF ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="dc089-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="dc089-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc089-107">EXAMPLES</span></span>

### <span data-ttu-id="dc089-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dc089-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="dc089-109">$resourceGroupName $policyName adındaki bir WAF ilkesi alın</span><span class="sxs-lookup"><span data-stu-id="dc089-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="dc089-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dc089-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="dc089-111">$resourceGroupName 'de tüm WAF ilkesini alın</span><span class="sxs-lookup"><span data-stu-id="dc089-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="dc089-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc089-112">PARAMETERS</span></span>

### <span data-ttu-id="dc089-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc089-113">-DefaultProfile</span></span>
<span data-ttu-id="dc089-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc089-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc089-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc089-115">-Name</span></span>
<span data-ttu-id="dc089-116">FireWallPolicy adı.</span><span class="sxs-lookup"><span data-stu-id="dc089-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="dc089-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc089-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc089-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dc089-118">The resource group name.</span></span>

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

### <span data-ttu-id="dc089-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc089-119">CommonParameters</span></span>
<span data-ttu-id="dc089-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc089-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc089-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dc089-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc089-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc089-122">INPUTS</span></span>

### <span data-ttu-id="dc089-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dc089-123">None</span></span>

## <span data-ttu-id="dc089-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc089-124">OUTPUTS</span></span>

### <span data-ttu-id="dc089-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="dc089-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="dc089-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc089-126">NOTES</span></span>

## <span data-ttu-id="dc089-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc089-127">RELATED LINKS</span></span>

<span data-ttu-id="dc089-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="dc089-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)</span></span>
