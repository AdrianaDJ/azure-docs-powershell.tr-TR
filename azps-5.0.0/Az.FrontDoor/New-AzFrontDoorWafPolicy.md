---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 441e47b4ef2a796fcdf5ee802cba83f0fce7e352
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277396"
---
# <span data-ttu-id="66baf-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="66baf-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="66baf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66baf-102">SYNOPSIS</span></span>
<span data-ttu-id="66baf-103">WAF İlkesi Oluştur</span><span class="sxs-lookup"><span data-stu-id="66baf-103">Create WAF policy</span></span>

## <span data-ttu-id="66baf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66baf-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66baf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66baf-105">DESCRIPTION</span></span>
<span data-ttu-id="66baf-106">**New-AzFrontDoorWafPolicy** cmdlet 'i, geçerli aboneliğin altındaki belirtilen kaynak grubunda yeni bir Azure WAF ilkesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="66baf-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="66baf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66baf-107">EXAMPLES</span></span>

### <span data-ttu-id="66baf-108">Örnek 1: WAF ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="66baf-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="66baf-109">WAF İlkesi Oluştur</span><span class="sxs-lookup"><span data-stu-id="66baf-109">Create WAF policy</span></span>

## <span data-ttu-id="66baf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66baf-110">PARAMETERS</span></span>

### <span data-ttu-id="66baf-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="66baf-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="66baf-112">Özel yanıt gövdesi</span><span class="sxs-lookup"><span data-stu-id="66baf-112">Custom Response Body</span></span>

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

### <span data-ttu-id="66baf-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="66baf-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="66baf-114">Özel yanıt durum kodu</span><span class="sxs-lookup"><span data-stu-id="66baf-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66baf-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="66baf-115">-Customrule</span></span>
<span data-ttu-id="66baf-116">İlkenin içindeki özel kurallar</span><span class="sxs-lookup"><span data-stu-id="66baf-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="66baf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66baf-117">-DefaultProfile</span></span>
<span data-ttu-id="66baf-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66baf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66baf-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="66baf-119">-EnabledState</span></span>
<span data-ttu-id="66baf-120">İlkenin etkin durumda veya devre dışı durumunda olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="66baf-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="66baf-121">Olası değerler: ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="66baf-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="66baf-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="66baf-122">-ManagedRule</span></span>
<span data-ttu-id="66baf-123">İlkenin içinde yönetilen kurallar</span><span class="sxs-lookup"><span data-stu-id="66baf-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="66baf-124">-Mod</span><span class="sxs-lookup"><span data-stu-id="66baf-124">-Mode</span></span>
<span data-ttu-id="66baf-125">Algılama modu 'nda veya koruma modu 'nun ilke düzeyinde olup olmadığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="66baf-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="66baf-126">Olası değerler: ' önlemeye yönelik ', ' algılama '</span><span class="sxs-lookup"><span data-stu-id="66baf-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="66baf-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="66baf-127">-Name</span></span>
<span data-ttu-id="66baf-128">WebApplicationFireWallPolicy Name.</span><span class="sxs-lookup"><span data-stu-id="66baf-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="66baf-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="66baf-129">-RedirectUrl</span></span>
<span data-ttu-id="66baf-130">Yönlendirme URL 'SI</span><span class="sxs-lookup"><span data-stu-id="66baf-130">Redirect URL</span></span>

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

### <span data-ttu-id="66baf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66baf-131">-ResourceGroupName</span></span>
<span data-ttu-id="66baf-132">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="66baf-132">The resource group name</span></span>

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

### <span data-ttu-id="66baf-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="66baf-133">-Confirm</span></span>
<span data-ttu-id="66baf-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66baf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66baf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66baf-135">-WhatIf</span></span>
<span data-ttu-id="66baf-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66baf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66baf-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66baf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66baf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66baf-138">CommonParameters</span></span>
<span data-ttu-id="66baf-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66baf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66baf-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="66baf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66baf-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66baf-141">INPUTS</span></span>

### <span data-ttu-id="66baf-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="66baf-142">None</span></span>

## <span data-ttu-id="66baf-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66baf-143">OUTPUTS</span></span>

### <span data-ttu-id="66baf-144">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="66baf-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="66baf-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66baf-145">NOTES</span></span>

## <span data-ttu-id="66baf-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66baf-146">RELATED LINKS</span></span>

<span data-ttu-id="66baf-147">[Güncelleştirme-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="66baf-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
