---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: 39325462d9c2cfb9c06296ff98e5595d2c2c2c06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107655"
---
# <span data-ttu-id="0c98d-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="0c98d-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="0c98d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c98d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c98d-103">Yönetim grubuna abonelik ekler.</span><span class="sxs-lookup"><span data-stu-id="0c98d-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="0c98d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c98d-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c98d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c98d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c98d-106">**New-AzManagementGroupSubscription** cmdlet 'ı bir yönetim grubuna abonelik ekler.</span><span class="sxs-lookup"><span data-stu-id="0c98d-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="0c98d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c98d-107">EXAMPLES</span></span>

### <span data-ttu-id="0c98d-108">Örnek 1: yönetim grubuna abonelik ekleme</span><span class="sxs-lookup"><span data-stu-id="0c98d-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="0c98d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c98d-109">PARAMETERS</span></span>

### <span data-ttu-id="0c98d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c98d-110">-DefaultProfile</span></span>
<span data-ttu-id="0c98d-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c98d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c98d-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="0c98d-112">-GroupName</span></span>
<span data-ttu-id="0c98d-113">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="0c98d-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c98d-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0c98d-114">-PassThru</span></span>
<span data-ttu-id="0c98d-115">`true`Başarılı yürütmeye dönme</span><span class="sxs-lookup"><span data-stu-id="0c98d-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="0c98d-116">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0c98d-116">-SubscriptionId</span></span>
<span data-ttu-id="0c98d-117">Yönetim ile ilişkili aboneliğin abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="0c98d-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c98d-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c98d-118">-Confirm</span></span>
<span data-ttu-id="0c98d-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c98d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c98d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c98d-120">-WhatIf</span></span>
<span data-ttu-id="0c98d-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c98d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c98d-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c98d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c98d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c98d-123">CommonParameters</span></span>
<span data-ttu-id="0c98d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c98d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c98d-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c98d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c98d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c98d-126">INPUTS</span></span>

### <span data-ttu-id="0c98d-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0c98d-127">None</span></span>

## <span data-ttu-id="0c98d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c98d-128">OUTPUTS</span></span>

### <span data-ttu-id="0c98d-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c98d-129">System.Boolean</span></span>

## <span data-ttu-id="0c98d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c98d-130">NOTES</span></span>

## <span data-ttu-id="0c98d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c98d-131">RELATED LINKS</span></span>
