---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: 882583c50db8a4b4473bce829aab120a68478434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587174"
---
# <span data-ttu-id="feb36-101">Remove-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="feb36-101">Remove-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="feb36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb36-102">SYNOPSIS</span></span>
<span data-ttu-id="feb36-103">Bir yönetim grubundan aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="feb36-103">Removes a Subscription from a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feb36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="feb36-104">SYNTAX</span></span>

```
Remove-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feb36-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="feb36-105">DESCRIPTION</span></span>
<span data-ttu-id="feb36-106">**Remove-AzureRmManagementGroupSubscription** cmdlet 'i, bir yönetim grubundan aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="feb36-106">The **Remove-AzureRmManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="feb36-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="feb36-107">EXAMPLES</span></span>

### <span data-ttu-id="feb36-108">Örnek 1-aboneliği yönetim grubundan kaldırın</span><span class="sxs-lookup"><span data-stu-id="feb36-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="feb36-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="feb36-109">PARAMETERS</span></span>

### <span data-ttu-id="feb36-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb36-110">-DefaultProfile</span></span>
<span data-ttu-id="feb36-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="feb36-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb36-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="feb36-112">-GroupName</span></span>
<span data-ttu-id="feb36-113">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="feb36-113">Management Group Id</span></span>

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

### <span data-ttu-id="feb36-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="feb36-114">-PassThru</span></span>
<span data-ttu-id="feb36-115">`true`Başarılı yürütmeye dönme</span><span class="sxs-lookup"><span data-stu-id="feb36-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="feb36-116">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="feb36-116">-SubscriptionId</span></span>
<span data-ttu-id="feb36-117">Yönetim ile ilişkilendirilmiş aboneliğin abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="feb36-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="feb36-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="feb36-118">-Confirm</span></span>
<span data-ttu-id="feb36-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="feb36-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feb36-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feb36-120">-WhatIf</span></span>
<span data-ttu-id="feb36-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="feb36-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feb36-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="feb36-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feb36-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb36-123">CommonParameters</span></span>
<span data-ttu-id="feb36-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="feb36-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb36-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb36-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb36-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="feb36-126">INPUTS</span></span>

### <span data-ttu-id="feb36-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="feb36-127">None</span></span>

## <span data-ttu-id="feb36-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="feb36-128">OUTPUTS</span></span>

### <span data-ttu-id="feb36-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="feb36-129">System.Boolean</span></span>

## <span data-ttu-id="feb36-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="feb36-130">NOTES</span></span>

## <span data-ttu-id="feb36-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="feb36-131">RELATED LINKS</span></span>
