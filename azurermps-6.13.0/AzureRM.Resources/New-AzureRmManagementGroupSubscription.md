---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: a3c75c653d75a4fde969672a245644ee04412731
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572629"
---
# <span data-ttu-id="8cc14-101">New-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="8cc14-101">New-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="8cc14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc14-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc14-103">Yönetim grubuna abonelik ekler.</span><span class="sxs-lookup"><span data-stu-id="8cc14-103">Adds a Subscription to a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cc14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8cc14-104">SYNTAX</span></span>

```
New-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc14-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8cc14-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc14-106">**Yeni-AzureRMManagementGroupSubscription** cmdlet 'ı bir yönetim grubuna abonelik ekler.</span><span class="sxs-lookup"><span data-stu-id="8cc14-106">The **New-AzureRMManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="8cc14-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8cc14-107">EXAMPLES</span></span>

### <span data-ttu-id="8cc14-108">Örnek 1: yönetim grubuna abonelik ekleme</span><span class="sxs-lookup"><span data-stu-id="8cc14-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzureRMManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="8cc14-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8cc14-109">PARAMETERS</span></span>

### <span data-ttu-id="8cc14-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc14-110">-DefaultProfile</span></span>
<span data-ttu-id="8cc14-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8cc14-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc14-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="8cc14-112">-GroupName</span></span>
<span data-ttu-id="8cc14-113">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="8cc14-113">Management Group Id</span></span>

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

### <span data-ttu-id="8cc14-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8cc14-114">-PassThru</span></span>
<span data-ttu-id="8cc14-115">`true`Başarılı yürütmeye dönme</span><span class="sxs-lookup"><span data-stu-id="8cc14-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="8cc14-116">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8cc14-116">-SubscriptionId</span></span>
<span data-ttu-id="8cc14-117">Yönetim ile ilişkilendirilmiş aboneliğin abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="8cc14-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="8cc14-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="8cc14-118">-Confirm</span></span>
<span data-ttu-id="8cc14-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8cc14-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc14-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc14-120">-WhatIf</span></span>
<span data-ttu-id="8cc14-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8cc14-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc14-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8cc14-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc14-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc14-123">CommonParameters</span></span>
<span data-ttu-id="8cc14-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8cc14-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc14-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc14-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc14-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8cc14-126">INPUTS</span></span>

### <span data-ttu-id="8cc14-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8cc14-127">None</span></span>

## <span data-ttu-id="8cc14-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8cc14-128">OUTPUTS</span></span>

### <span data-ttu-id="8cc14-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8cc14-129">System.Boolean</span></span>

## <span data-ttu-id="8cc14-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8cc14-130">NOTES</span></span>

## <span data-ttu-id="8cc14-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8cc14-131">RELATED LINKS</span></span>
