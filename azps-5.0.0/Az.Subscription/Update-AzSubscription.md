---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277971"
---
# <span data-ttu-id="a7dbe-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="a7dbe-101">Update-AzSubscription</span></span>

## <span data-ttu-id="a7dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="a7dbe-103">Azure aboneliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a7dbe-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="a7dbe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7dbe-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7dbe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="a7dbe-106">**Update-Azabonelik** cmdlet 'ı bir Azure aboneliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a7dbe-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="a7dbe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7dbe-107">EXAMPLES</span></span>

### <span data-ttu-id="a7dbe-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7dbe-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="a7dbe-109">Aboneliği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a7dbe-109">Updates the subscription</span></span>

## <span data-ttu-id="a7dbe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7dbe-110">PARAMETERS</span></span>

### <span data-ttu-id="a7dbe-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="a7dbe-111">-Action</span></span>
<span data-ttu-id="a7dbe-112">Abonelikte gerçekleştirilecek eylem</span><span class="sxs-lookup"><span data-stu-id="a7dbe-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="a7dbe-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a7dbe-113">-AsJob</span></span>
<span data-ttu-id="a7dbe-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a7dbe-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7dbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7dbe-115">-DefaultProfile</span></span>
<span data-ttu-id="a7dbe-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7dbe-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7dbe-117">-Name</span></span>
<span data-ttu-id="a7dbe-118">Aboneliğin adı</span><span class="sxs-lookup"><span data-stu-id="a7dbe-118">Name of the subscription</span></span>

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

### <span data-ttu-id="a7dbe-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a7dbe-119">-SubscriptionId</span></span>
<span data-ttu-id="a7dbe-120">Güncelleştirilecek abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="a7dbe-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="a7dbe-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7dbe-121">-Confirm</span></span>
<span data-ttu-id="a7dbe-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7dbe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7dbe-123">-WhatIf</span></span>
<span data-ttu-id="a7dbe-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7dbe-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7dbe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7dbe-126">CommonParameters</span></span>
<span data-ttu-id="a7dbe-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7dbe-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a7dbe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7dbe-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7dbe-129">INPUTS</span></span>

### <span data-ttu-id="a7dbe-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a7dbe-130">None</span></span>

## <span data-ttu-id="a7dbe-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7dbe-131">OUTPUTS</span></span>

### <span data-ttu-id="a7dbe-132">Microsoft. Azure. Commands. Subscription. modeller. psazuyeniden gönderme komutları</span><span class="sxs-lookup"><span data-stu-id="a7dbe-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a7dbe-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7dbe-133">NOTES</span></span>

## <span data-ttu-id="a7dbe-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7dbe-134">RELATED LINKS</span></span>
