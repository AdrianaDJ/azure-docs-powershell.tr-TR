---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762930"
---
# <span data-ttu-id="4c2ea-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4c2ea-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="4c2ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="4c2ea-103">WAF ilkesi oluşturma için ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c2ea-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c2ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c2ea-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c2ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c2ea-105">DESCRIPTION</span></span>
<span data-ttu-id="4c2ea-106">WAF ilkesi oluşturma için ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c2ea-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="4c2ea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c2ea-107">EXAMPLES</span></span>

### <span data-ttu-id="4c2ea-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4c2ea-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="4c2ea-109">ManagedRule nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c2ea-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="4c2ea-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c2ea-110">PARAMETERS</span></span>

### <span data-ttu-id="4c2ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c2ea-111">-DefaultProfile</span></span>
<span data-ttu-id="4c2ea-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c2ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c2ea-113">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="4c2ea-113">-Priority</span></span>
<span data-ttu-id="4c2ea-114">Kuralın önceliğini açıklar</span><span class="sxs-lookup"><span data-stu-id="4c2ea-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2ea-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4c2ea-115">-RuleGroupOverride</span></span>
<span data-ttu-id="4c2ea-116">Azure yönetilen sağlayıcısı geçersiz kılma yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="4c2ea-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2ea-117">-Version</span><span class="sxs-lookup"><span data-stu-id="4c2ea-117">-Version</span></span>
<span data-ttu-id="4c2ea-118">RuleSet 'in sürümü</span><span class="sxs-lookup"><span data-stu-id="4c2ea-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="4c2ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c2ea-119">CommonParameters</span></span>
<span data-ttu-id="4c2ea-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c2ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c2ea-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c2ea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c2ea-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c2ea-122">INPUTS</span></span>

### <span data-ttu-id="4c2ea-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4c2ea-123">None</span></span>

## <span data-ttu-id="4c2ea-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c2ea-124">OUTPUTS</span></span>

### <span data-ttu-id="4c2ea-125">Microsoft. Azure. Commands. Frontkapısı. modeller. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="4c2ea-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="4c2ea-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c2ea-126">NOTES</span></span>

## <span data-ttu-id="4c2ea-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c2ea-127">RELATED LINKS</span></span>

<span data-ttu-id="4c2ea-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="4c2ea-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
