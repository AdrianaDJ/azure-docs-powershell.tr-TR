---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322037"
---
# <span data-ttu-id="5efc4-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="5efc4-101">Remove-AzContext</span></span>

## <span data-ttu-id="5efc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5efc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5efc4-103">Kullanılabilir içerik kümesinden bağlam kaldırma</span><span class="sxs-lookup"><span data-stu-id="5efc4-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="5efc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5efc4-104">SYNTAX</span></span>

### <span data-ttu-id="5efc4-105">RemoveByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5efc4-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5efc4-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="5efc4-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="5efc4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5efc4-107">DESCRIPTION</span></span>
<span data-ttu-id="5efc4-108">Bağlam kümesinden bir Azure bağlamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5efc4-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="5efc4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5efc4-109">EXAMPLES</span></span>

### <span data-ttu-id="5efc4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5efc4-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="5efc4-111">Varsayılan adlı bağlamı kaldırın</span><span class="sxs-lookup"><span data-stu-id="5efc4-111">Remove the context named default</span></span>

## <span data-ttu-id="5efc4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5efc4-112">PARAMETERS</span></span>

### <span data-ttu-id="5efc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5efc4-113">-DefaultProfile</span></span>
<span data-ttu-id="5efc4-114">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5efc4-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5efc4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5efc4-115">-Force</span></span>
<span data-ttu-id="5efc4-116">Varsayılan değer olsa bile içeriği kaldır</span><span class="sxs-lookup"><span data-stu-id="5efc4-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="5efc4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5efc4-117">-InputObject</span></span>
<span data-ttu-id="5efc4-118">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5efc4-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5efc4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5efc4-119">-Name</span></span>
<span data-ttu-id="5efc4-120">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="5efc4-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5efc4-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5efc4-121">-PassThru</span></span>
<span data-ttu-id="5efc4-122">Kaldırılan içeriği döndürme</span><span class="sxs-lookup"><span data-stu-id="5efc4-122">Return the removed context</span></span>

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

### <span data-ttu-id="5efc4-123">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="5efc4-123">-Scope</span></span>
<span data-ttu-id="5efc4-124">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="5efc4-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="5efc4-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="5efc4-125">-Confirm</span></span>
<span data-ttu-id="5efc4-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5efc4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5efc4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5efc4-127">-WhatIf</span></span>
<span data-ttu-id="5efc4-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5efc4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5efc4-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5efc4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5efc4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5efc4-130">CommonParameters</span></span>
<span data-ttu-id="5efc4-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5efc4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5efc4-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5efc4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5efc4-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5efc4-133">INPUTS</span></span>

### <span data-ttu-id="5efc4-134">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="5efc4-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="5efc4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5efc4-135">OUTPUTS</span></span>

### <span data-ttu-id="5efc4-136">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="5efc4-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="5efc4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5efc4-137">NOTES</span></span>

## <span data-ttu-id="5efc4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5efc4-138">RELATED LINKS</span></span>
