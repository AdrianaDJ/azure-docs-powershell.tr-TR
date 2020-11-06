---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 0e102d6c0c4db5bd3d93d4349a2a0e06284cd8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590091"
---
# <span data-ttu-id="36107-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="36107-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="36107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36107-102">SYNOPSIS</span></span>
<span data-ttu-id="36107-103">Kullanılabilir içerik kümesinden bağlam kaldırma</span><span class="sxs-lookup"><span data-stu-id="36107-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36107-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36107-104">SYNTAX</span></span>

### <span data-ttu-id="36107-105">RemoveByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36107-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36107-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="36107-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="36107-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="36107-107">DESCRIPTION</span></span>
<span data-ttu-id="36107-108">Bağlam kümesinden bir Azure bağlamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="36107-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="36107-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36107-109">EXAMPLES</span></span>

### <span data-ttu-id="36107-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36107-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="36107-111">Varsayılan adlı bağlamı kaldırın</span><span class="sxs-lookup"><span data-stu-id="36107-111">Remove the context named default</span></span>

## <span data-ttu-id="36107-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36107-112">PARAMETERS</span></span>

### <span data-ttu-id="36107-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36107-113">-DefaultProfile</span></span>
<span data-ttu-id="36107-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36107-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36107-115">-Force</span><span class="sxs-lookup"><span data-stu-id="36107-115">-Force</span></span>
<span data-ttu-id="36107-116">Kısayol olsa bile içeriği kaldır</span><span class="sxs-lookup"><span data-stu-id="36107-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="36107-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36107-117">-InputObject</span></span>
<span data-ttu-id="36107-118">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="36107-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36107-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="36107-119">-Name</span></span>
<span data-ttu-id="36107-120">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="36107-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36107-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="36107-121">-PassThru</span></span>
<span data-ttu-id="36107-122">Kaldırılan içeriği döndürme</span><span class="sxs-lookup"><span data-stu-id="36107-122">Return the removed context</span></span>

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

### <span data-ttu-id="36107-123">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="36107-123">-Scope</span></span>
<span data-ttu-id="36107-124">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="36107-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36107-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="36107-125">-Confirm</span></span>
<span data-ttu-id="36107-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36107-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36107-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36107-127">-WhatIf</span></span>
<span data-ttu-id="36107-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36107-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36107-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36107-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36107-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36107-130">CommonParameters</span></span>
<span data-ttu-id="36107-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36107-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36107-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36107-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36107-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36107-133">INPUTS</span></span>

### <span data-ttu-id="36107-134">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="36107-134">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="36107-135">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36107-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="36107-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36107-136">OUTPUTS</span></span>

### <span data-ttu-id="36107-137">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="36107-137">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="36107-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36107-138">NOTES</span></span>

## <span data-ttu-id="36107-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36107-139">RELATED LINKS</span></span>
