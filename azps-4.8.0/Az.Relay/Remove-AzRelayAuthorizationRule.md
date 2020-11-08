---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109355"
---
# <span data-ttu-id="272a1-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="272a1-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="272a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="272a1-102">SYNOPSIS</span></span>
<span data-ttu-id="272a1-103">Verilen geçiş varlıklarından (Namespace/WcfRelay/HybridConnection) bir HybridConnection kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="272a1-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="272a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="272a1-104">SYNTAX</span></span>

### <span data-ttu-id="272a1-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="272a1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="272a1-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="272a1-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="272a1-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="272a1-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="272a1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="272a1-108">DESCRIPTION</span></span>
<span data-ttu-id="272a1-109">**Remove-AzRelayAuthorizationRule** cmdlet 'i, verilen geçiş varlıklarının yetkilendirme kuralını (Namespace/WcfRelay/HybridConnection) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="272a1-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="272a1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="272a1-110">EXAMPLES</span></span>

### <span data-ttu-id="272a1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="272a1-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="272a1-112">Ad alanının yetkilendirme kuralını kaldırır `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="272a1-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="272a1-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="272a1-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="272a1-114">`AuthoRule1`WcfRelay 'in kimlik alanındaki yetkilendirme kuralını kaldırır `TestWcfRelay` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="272a1-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="272a1-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="272a1-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="272a1-116">Çalışma `AuthoRule1` alanından HybridConnection 'un yetkilendirme kuralını kaldırır `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="272a1-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="272a1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="272a1-117">PARAMETERS</span></span>

### <span data-ttu-id="272a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272a1-118">-DefaultProfile</span></span>
<span data-ttu-id="272a1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="272a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="272a1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="272a1-120">-Force</span></span>
<span data-ttu-id="272a1-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="272a1-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272a1-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="272a1-122">-HybridConnection</span></span>
<span data-ttu-id="272a1-123">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="272a1-123">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272a1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="272a1-124">-Name</span></span>
<span data-ttu-id="272a1-125">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="272a1-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272a1-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="272a1-126">-Namespace</span></span>
<span data-ttu-id="272a1-127">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="272a1-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272a1-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="272a1-128">-PassThru</span></span>
<span data-ttu-id="272a1-129">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="272a1-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272a1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272a1-130">-ResourceGroupName</span></span>
<span data-ttu-id="272a1-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="272a1-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272a1-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="272a1-132">-WcfRelay</span></span>
<span data-ttu-id="272a1-133">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="272a1-133">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="272a1-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="272a1-134">-Confirm</span></span>
<span data-ttu-id="272a1-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="272a1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="272a1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="272a1-136">-WhatIf</span></span>
<span data-ttu-id="272a1-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="272a1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="272a1-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="272a1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="272a1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272a1-139">CommonParameters</span></span>
<span data-ttu-id="272a1-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="272a1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272a1-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272a1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272a1-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="272a1-142">INPUTS</span></span>

### <span data-ttu-id="272a1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="272a1-143">System.String</span></span>

## <span data-ttu-id="272a1-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="272a1-144">OUTPUTS</span></span>

### <span data-ttu-id="272a1-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="272a1-145">System.Boolean</span></span>

## <span data-ttu-id="272a1-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="272a1-146">NOTES</span></span>

## <span data-ttu-id="272a1-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="272a1-147">RELATED LINKS</span></span>
