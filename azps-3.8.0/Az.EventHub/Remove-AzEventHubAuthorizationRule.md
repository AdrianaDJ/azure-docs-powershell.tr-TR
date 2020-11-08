---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937530"
---
# <span data-ttu-id="696fb-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="696fb-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="696fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696fb-102">SYNOPSIS</span></span>
<span data-ttu-id="696fb-103">Belirtilen olay hub yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="696fb-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="696fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="696fb-104">SYNTAX</span></span>

### <span data-ttu-id="696fb-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="696fb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="696fb-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="696fb-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="696fb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="696fb-107">DESCRIPTION</span></span>
<span data-ttu-id="696fb-108">Remove-AzEventHubAuthorizationRule cmdlet 'i, verilen olay hub 'ından belirtilen yetkilendirme kuralını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="696fb-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="696fb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="696fb-109">EXAMPLES</span></span>

### <span data-ttu-id="696fb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="696fb-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="696fb-111">\`Myauthrulename \` 'ı ad alanı adından kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="696fb-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="696fb-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="696fb-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="696fb-113">\`Cyauthrulename yetkilendirme kuralını, \` Olay Hub \` myeventhubname ' den kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="696fb-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="696fb-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="696fb-114">PARAMETERS</span></span>

### <span data-ttu-id="696fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696fb-115">-DefaultProfile</span></span>
<span data-ttu-id="696fb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="696fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="696fb-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="696fb-117">-EventHub</span></span>
<span data-ttu-id="696fb-118">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="696fb-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696fb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="696fb-119">-Force</span></span>
<span data-ttu-id="696fb-120">Onay sorma</span><span class="sxs-lookup"><span data-stu-id="696fb-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="696fb-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="696fb-121">-Name</span></span>
<span data-ttu-id="696fb-122">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="696fb-122">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696fb-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="696fb-123">-Namespace</span></span>
<span data-ttu-id="696fb-124">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="696fb-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696fb-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="696fb-125">-PassThru</span></span>
<span data-ttu-id="696fb-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="696fb-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="696fb-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="696fb-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="696fb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696fb-128">-ResourceGroupName</span></span>
<span data-ttu-id="696fb-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="696fb-129">Resource Group Name</span></span>

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

### <span data-ttu-id="696fb-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="696fb-130">-Confirm</span></span>
<span data-ttu-id="696fb-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="696fb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="696fb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696fb-132">-WhatIf</span></span>
<span data-ttu-id="696fb-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="696fb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="696fb-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="696fb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="696fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696fb-135">CommonParameters</span></span>
<span data-ttu-id="696fb-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="696fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696fb-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696fb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696fb-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="696fb-138">INPUTS</span></span>

### <span data-ttu-id="696fb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="696fb-139">System.String</span></span>

## <span data-ttu-id="696fb-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="696fb-140">OUTPUTS</span></span>

### <span data-ttu-id="696fb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="696fb-141">System.Boolean</span></span>

## <span data-ttu-id="696fb-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="696fb-142">NOTES</span></span>

## <span data-ttu-id="696fb-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="696fb-143">RELATED LINKS</span></span>