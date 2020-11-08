---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274953"
---
# <span data-ttu-id="8fc0d-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="8fc0d-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="8fc0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc0d-103">WAF ilkesini alın</span><span class="sxs-lookup"><span data-stu-id="8fc0d-103">Get WAF policy</span></span>

## <span data-ttu-id="8fc0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fc0d-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fc0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fc0d-105">DESCRIPTION</span></span>
<span data-ttu-id="8fc0d-106">**Get-AzFrontDoorWafPolicy** cmdletGet, geçerli aboneliğin altındaki bir kaynak grubundaki WAF ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="8fc0d-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="8fc0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fc0d-107">EXAMPLES</span></span>

### <span data-ttu-id="8fc0d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8fc0d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="8fc0d-109">$resourceGroupName $policyName adındaki bir WAF ilkesi alın</span><span class="sxs-lookup"><span data-stu-id="8fc0d-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="8fc0d-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8fc0d-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="8fc0d-111">$resourceGroupName 'de tüm WAF ilkesini alın</span><span class="sxs-lookup"><span data-stu-id="8fc0d-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="8fc0d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fc0d-112">PARAMETERS</span></span>

### <span data-ttu-id="8fc0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc0d-113">-DefaultProfile</span></span>
<span data-ttu-id="8fc0d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc0d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8fc0d-115">-Name</span></span>
<span data-ttu-id="8fc0d-116">FireWallPolicy adı.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="8fc0d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc0d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8fc0d-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-118">The resource group name.</span></span>

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

### <span data-ttu-id="8fc0d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc0d-119">CommonParameters</span></span>
<span data-ttu-id="8fc0d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc0d-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc0d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fc0d-122">INPUTS</span></span>

### <span data-ttu-id="8fc0d-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8fc0d-123">None</span></span>

## <span data-ttu-id="8fc0d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fc0d-124">OUTPUTS</span></span>

### <span data-ttu-id="8fc0d-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8fc0d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="8fc0d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fc0d-126">NOTES</span></span>

## <span data-ttu-id="8fc0d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fc0d-127">RELATED LINKS</span></span>

<span data-ttu-id="8fc0d-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Güncelleştirme-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="8fc0d-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
