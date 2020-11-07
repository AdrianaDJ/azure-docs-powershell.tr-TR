---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: e5a7d0a8e7d000e9d4bdceae41d05990a93c71a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759342"
---
# <span data-ttu-id="2ff1d-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="2ff1d-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="2ff1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff1d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff1d-103">Bir yönetim grubundan aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ff1d-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="2ff1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ff1d-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ff1d-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff1d-106">**Remove-AzManagementGroupSubscription** cmdlet 'ı bir yönetim grubundan aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ff1d-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="2ff1d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ff1d-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff1d-108">Örnek 1-aboneliği yönetim grubundan kaldırın</span><span class="sxs-lookup"><span data-stu-id="2ff1d-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="2ff1d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ff1d-109">PARAMETERS</span></span>

### <span data-ttu-id="2ff1d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff1d-110">-DefaultProfile</span></span>
<span data-ttu-id="2ff1d-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ff1d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff1d-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="2ff1d-112">-GroupName</span></span>
<span data-ttu-id="2ff1d-113">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="2ff1d-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff1d-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2ff1d-114">-PassThru</span></span>
<span data-ttu-id="2ff1d-115">`true`Başarılı yürütmeye dönme</span><span class="sxs-lookup"><span data-stu-id="2ff1d-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="2ff1d-116">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2ff1d-116">-SubscriptionId</span></span>
<span data-ttu-id="2ff1d-117">Yönetim ile ilişkilendirilmiş aboneliğin abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="2ff1d-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="2ff1d-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ff1d-118">-Confirm</span></span>
<span data-ttu-id="2ff1d-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ff1d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff1d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff1d-120">-WhatIf</span></span>
<span data-ttu-id="2ff1d-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ff1d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff1d-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ff1d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff1d-123">CommonParameters</span></span>
<span data-ttu-id="2ff1d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ff1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff1d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff1d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff1d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ff1d-126">INPUTS</span></span>

### <span data-ttu-id="2ff1d-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2ff1d-127">None</span></span>

## <span data-ttu-id="2ff1d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ff1d-128">OUTPUTS</span></span>

### <span data-ttu-id="2ff1d-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ff1d-129">System.Boolean</span></span>

## <span data-ttu-id="2ff1d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ff1d-130">NOTES</span></span>

## <span data-ttu-id="2ff1d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ff1d-131">RELATED LINKS</span></span>
