---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 8eaf2ff99fe7f3ea49d73af95eb4482c645be59f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763634"
---
# <span data-ttu-id="7fb5f-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7fb5f-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="7fb5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb5f-103">Verilen geçiş varlıklarından (Namespace/WcfRelay/HybridConnection) bir HybridConnection kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fb5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fb5f-104">SYNTAX</span></span>

### <span data-ttu-id="7fb5f-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7fb5f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb5f-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fb5f-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fb5f-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7fb5f-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb5f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fb5f-108">DESCRIPTION</span></span>
<span data-ttu-id="7fb5f-109">**Remove-AzureRmRelayAuthorizationRule** cmdlet 'i, verilen geçiş varlıklarının (Namespace/WcfRelay/HybridConnection) yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7fb5f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fb5f-110">EXAMPLES</span></span>

### <span data-ttu-id="7fb5f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7fb5f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="7fb5f-112">Ad alanının yetkilendirme kuralını kaldırır `AuthoRule1` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="7fb5f-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="7fb5f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7fb5f-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="7fb5f-114">`AuthoRule1`WcfRelay 'in kimlik alanındaki yetkilendirme kuralını kaldırır `TestWcfRelay` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="7fb5f-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="7fb5f-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7fb5f-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="7fb5f-116">Çalışma `AuthoRule1` alanından HybridConnection 'un yetkilendirme kuralını kaldırır `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="7fb5f-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="7fb5f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fb5f-117">PARAMETERS</span></span>

### <span data-ttu-id="7fb5f-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="7fb5f-118">-Confirm</span></span>
<span data-ttu-id="7fb5f-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb5f-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7fb5f-120">-HybridConnection</span></span>
<span data-ttu-id="7fb5f-121">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="7fb5f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7fb5f-122">-Name</span></span>
<span data-ttu-id="7fb5f-123">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7fb5f-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7fb5f-124">-Namespace</span></span>
<span data-ttu-id="7fb5f-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-125">Namespace Name.</span></span>

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

### <span data-ttu-id="7fb5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="7fb5f-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7fb5f-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7fb5f-128">-WcfRelay</span></span>
<span data-ttu-id="7fb5f-129">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="7fb5f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb5f-130">-WhatIf</span></span>
<span data-ttu-id="7fb5f-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb5f-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb5f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb5f-133">-DefaultProfile</span></span>
<span data-ttu-id="7fb5f-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fb5f-135">-Force</span><span class="sxs-lookup"><span data-stu-id="7fb5f-135">-Force</span></span>
<span data-ttu-id="7fb5f-136">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7fb5f-137">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7fb5f-137">-PassThru</span></span>
<span data-ttu-id="7fb5f-138">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="7fb5f-138">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7fb5f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb5f-139">CommonParameters</span></span>
<span data-ttu-id="7fb5f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fb5f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb5f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb5f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb5f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fb5f-142">INPUTS</span></span>

### <span data-ttu-id="7fb5f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7fb5f-143">System.String</span></span>

## <span data-ttu-id="7fb5f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fb5f-144">OUTPUTS</span></span>

### <span data-ttu-id="7fb5f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fb5f-145">System.Boolean</span></span>

## <span data-ttu-id="7fb5f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fb5f-146">NOTES</span></span>

## <span data-ttu-id="7fb5f-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fb5f-147">RELATED LINKS</span></span>

