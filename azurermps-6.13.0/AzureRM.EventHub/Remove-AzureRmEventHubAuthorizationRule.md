---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762615"
---
# <span data-ttu-id="6541a-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6541a-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="6541a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6541a-102">SYNOPSIS</span></span>
<span data-ttu-id="6541a-103">Belirtilen olay hub yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6541a-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6541a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6541a-104">SYNTAX</span></span>

### <span data-ttu-id="6541a-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6541a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6541a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6541a-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6541a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6541a-107">DESCRIPTION</span></span>
<span data-ttu-id="6541a-108">Remove-AzureRmEventHubAuthorizationRule cmdlet 'i, verilen olay hub 'ından belirtilen yetkilendirme kuralını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="6541a-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="6541a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6541a-109">EXAMPLES</span></span>

### <span data-ttu-id="6541a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6541a-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="6541a-111">\`Myauthrulename \` 'ı ad alanı adından kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="6541a-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="6541a-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6541a-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="6541a-113">\`Cyauthrulename yetkilendirme kuralını, \` Olay Hub \` myeventhubname ' den kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="6541a-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="6541a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6541a-114">PARAMETERS</span></span>

### <span data-ttu-id="6541a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6541a-115">-DefaultProfile</span></span>
<span data-ttu-id="6541a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6541a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6541a-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6541a-117">-EventHub</span></span>
<span data-ttu-id="6541a-118">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="6541a-118">EventHub Name</span></span>

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

### <span data-ttu-id="6541a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6541a-119">-Force</span></span>
<span data-ttu-id="6541a-120">Onay sorma</span><span class="sxs-lookup"><span data-stu-id="6541a-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="6541a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6541a-121">-Name</span></span>
<span data-ttu-id="6541a-122">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="6541a-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="6541a-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6541a-123">-Namespace</span></span>
<span data-ttu-id="6541a-124">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="6541a-124">Namespace Name</span></span>

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

### <span data-ttu-id="6541a-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6541a-125">-PassThru</span></span>
<span data-ttu-id="6541a-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6541a-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6541a-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6541a-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6541a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6541a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6541a-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6541a-129">Resource Group Name</span></span>

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

### <span data-ttu-id="6541a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="6541a-130">-Confirm</span></span>
<span data-ttu-id="6541a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6541a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6541a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6541a-132">-WhatIf</span></span>
<span data-ttu-id="6541a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6541a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6541a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6541a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6541a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6541a-135">CommonParameters</span></span>
<span data-ttu-id="6541a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6541a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6541a-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6541a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6541a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6541a-138">INPUTS</span></span>

### <span data-ttu-id="6541a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6541a-139">System.String</span></span>

## <span data-ttu-id="6541a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6541a-140">OUTPUTS</span></span>

### <span data-ttu-id="6541a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6541a-141">System.Boolean</span></span>

## <span data-ttu-id="6541a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6541a-142">NOTES</span></span>

## <span data-ttu-id="6541a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6541a-143">RELATED LINKS</span></span>
