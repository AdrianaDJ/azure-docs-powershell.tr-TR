---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: b3983d63beecb7d5a45f31409758b98aa64786a3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936396"
---
# <span data-ttu-id="23fbc-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="23fbc-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="23fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="23fbc-103">Yönetim grubuna abonelik ekler.</span><span class="sxs-lookup"><span data-stu-id="23fbc-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="23fbc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23fbc-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23fbc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="23fbc-106">**New-AzManagementGroupSubscription** cmdlet 'ı bir yönetim grubuna abonelik ekler.</span><span class="sxs-lookup"><span data-stu-id="23fbc-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="23fbc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23fbc-107">EXAMPLES</span></span>

### <span data-ttu-id="23fbc-108">Örnek 1: yönetim grubuna abonelik ekleme</span><span class="sxs-lookup"><span data-stu-id="23fbc-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="23fbc-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23fbc-109">PARAMETERS</span></span>

### <span data-ttu-id="23fbc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fbc-110">-DefaultProfile</span></span>
<span data-ttu-id="23fbc-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23fbc-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23fbc-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="23fbc-112">-GroupName</span></span>
<span data-ttu-id="23fbc-113">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="23fbc-113">Management Group Id</span></span>

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

### <span data-ttu-id="23fbc-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="23fbc-114">-PassThru</span></span>
<span data-ttu-id="23fbc-115">`true`Başarılı yürütmeye dönme</span><span class="sxs-lookup"><span data-stu-id="23fbc-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="23fbc-116">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="23fbc-116">-SubscriptionId</span></span>
<span data-ttu-id="23fbc-117">Yönetim ile ilişkilendirilmiş aboneliğin abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="23fbc-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="23fbc-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="23fbc-118">-Confirm</span></span>
<span data-ttu-id="23fbc-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23fbc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23fbc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23fbc-120">-WhatIf</span></span>
<span data-ttu-id="23fbc-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23fbc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23fbc-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23fbc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23fbc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fbc-123">CommonParameters</span></span>
<span data-ttu-id="23fbc-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23fbc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fbc-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fbc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fbc-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23fbc-126">INPUTS</span></span>

### <span data-ttu-id="23fbc-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="23fbc-127">None</span></span>

## <span data-ttu-id="23fbc-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23fbc-128">OUTPUTS</span></span>

### <span data-ttu-id="23fbc-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23fbc-129">System.Boolean</span></span>

## <span data-ttu-id="23fbc-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23fbc-130">NOTES</span></span>

## <span data-ttu-id="23fbc-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23fbc-131">RELATED LINKS</span></span>
