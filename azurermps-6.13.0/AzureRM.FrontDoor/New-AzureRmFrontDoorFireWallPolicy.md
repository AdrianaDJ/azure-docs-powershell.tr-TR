---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: b18f17830dd08f95c3d887ce272ff31e080001a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594412"
---
# <span data-ttu-id="28463-101">New-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="28463-101">New-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="28463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28463-102">SYNOPSIS</span></span>
<span data-ttu-id="28463-103">WAF İlkesi Oluştur</span><span class="sxs-lookup"><span data-stu-id="28463-103">Create WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28463-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28463-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28463-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="28463-105">DESCRIPTION</span></span>
<span data-ttu-id="28463-106">**New-AzureRmFrontDoorFireWallPolicy** cmdlet 'i, geçerli aboneliğin altındaki belirtilen kaynak grubunda yeni bir Azure WAF ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="28463-106">The **New-AzureRmFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="28463-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28463-107">EXAMPLES</span></span>

### <span data-ttu-id="28463-108">Örnek 1: WAF ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="28463-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroupName -Customrule $customRule1 -ManagedRule $managedRule1 -En
abledState Enabled -Mode Prevention


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

<span data-ttu-id="28463-109">WAF İlkesi Oluştur</span><span class="sxs-lookup"><span data-stu-id="28463-109">Create WAF policy</span></span>

## <span data-ttu-id="28463-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28463-110">PARAMETERS</span></span>

### <span data-ttu-id="28463-111">-Customrule</span><span class="sxs-lookup"><span data-stu-id="28463-111">-Customrule</span></span>
<span data-ttu-id="28463-112">İlkenin içindeki özel kurallar</span><span class="sxs-lookup"><span data-stu-id="28463-112">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28463-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28463-113">-DefaultProfile</span></span>
<span data-ttu-id="28463-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28463-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28463-115">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="28463-115">-EnabledState</span></span>
<span data-ttu-id="28463-116">İlkenin etkin durumda veya devre dışı durumunda olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="28463-116">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="28463-117">Olası değerler: ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="28463-117">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28463-118">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="28463-118">-ManagedRule</span></span>
<span data-ttu-id="28463-119">İlkenin içinde yönetilen kurallar</span><span class="sxs-lookup"><span data-stu-id="28463-119">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28463-120">-Mod</span><span class="sxs-lookup"><span data-stu-id="28463-120">-Mode</span></span>
<span data-ttu-id="28463-121">Algılama modu 'nda veya koruma modu 'nun ilke düzeyinde olup olmadığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="28463-121">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="28463-122">Olası değerler: ' önlemeye yönelik ', ' algılama '</span><span class="sxs-lookup"><span data-stu-id="28463-122">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28463-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="28463-123">-Name</span></span>
<span data-ttu-id="28463-124">WebApplicationFireWallPolicy Name.</span><span class="sxs-lookup"><span data-stu-id="28463-124">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="28463-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28463-125">-ResourceGroupName</span></span>
<span data-ttu-id="28463-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="28463-126">The resource group name</span></span>

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

### <span data-ttu-id="28463-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="28463-127">-Confirm</span></span>
<span data-ttu-id="28463-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28463-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28463-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28463-129">-WhatIf</span></span>
<span data-ttu-id="28463-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28463-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28463-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28463-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28463-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28463-132">CommonParameters</span></span>
<span data-ttu-id="28463-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28463-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28463-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28463-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28463-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28463-135">INPUTS</span></span>

### <span data-ttu-id="28463-136">System. String</span><span class="sxs-lookup"><span data-stu-id="28463-136">System.String</span></span>

## <span data-ttu-id="28463-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28463-137">OUTPUTS</span></span>

### <span data-ttu-id="28463-138">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="28463-138">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="28463-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28463-139">NOTES</span></span>

## <span data-ttu-id="28463-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28463-140">RELATED LINKS</span></span>

<span data-ttu-id="28463-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="28463-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
