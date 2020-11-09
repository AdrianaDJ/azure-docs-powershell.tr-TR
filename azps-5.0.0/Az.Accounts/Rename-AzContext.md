---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 09c0faec1ab424ef1bfb10fec35dd59646e4711c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322033"
---
# <span data-ttu-id="3efc2-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="3efc2-101">Rename-AzContext</span></span>

## <span data-ttu-id="3efc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3efc2-102">SYNOPSIS</span></span>
<span data-ttu-id="3efc2-103">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="3efc2-103">Rename an Azure context.</span></span>  <span data-ttu-id="3efc2-104">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="3efc2-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="3efc2-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3efc2-105">SYNTAX</span></span>

### <span data-ttu-id="3efc2-106">RenameByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3efc2-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="3efc2-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="3efc2-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="3efc2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3efc2-108">DESCRIPTION</span></span>
<span data-ttu-id="3efc2-109">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="3efc2-109">Rename an Azure context.</span></span>  <span data-ttu-id="3efc2-110">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="3efc2-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="3efc2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3efc2-111">EXAMPLES</span></span>

### <span data-ttu-id="3efc2-112">Örnek 1: adlandırılmış parametreleri kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="3efc2-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="3efc2-113">' user1@contoso.org ' ' 12345-6789-2345-3567890 ' aboneliği ile ' ' çalışma '</span><span class="sxs-lookup"><span data-stu-id="3efc2-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="3efc2-114">Bu komuttan sonra, ' Select-AzContext çalışması ' kullanarak bağlamı hedefleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3efc2-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="3efc2-115">Sekme tamamlamayı kullanarak ' SourceName ' değerleri arasında sekme alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3efc2-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="3efc2-116">Örnek 2: konum parametrelerini kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="3efc2-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="3efc2-117">"My Context" adlı bağlamı "Iş" olarak yeniden adlandırın.</span><span class="sxs-lookup"><span data-stu-id="3efc2-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="3efc2-118">Bu komuttan sonra, Select-AzContext Iş kullanarak bağlam hedefleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3efc2-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="3efc2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3efc2-119">PARAMETERS</span></span>

### <span data-ttu-id="3efc2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3efc2-120">-DefaultProfile</span></span>
<span data-ttu-id="3efc2-121">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3efc2-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3efc2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3efc2-122">-Force</span></span>
<span data-ttu-id="3efc2-123">Hedef bağlamı zaten var olsa bile içeriği yeniden adlandır</span><span class="sxs-lookup"><span data-stu-id="3efc2-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="3efc2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3efc2-124">-InputObject</span></span>
<span data-ttu-id="3efc2-125">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3efc2-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3efc2-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3efc2-126">-PassThru</span></span>
<span data-ttu-id="3efc2-127">Yeniden adlandırılan bağlamı döndür.</span><span class="sxs-lookup"><span data-stu-id="3efc2-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="3efc2-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="3efc2-128">-Scope</span></span>
<span data-ttu-id="3efc2-129">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="3efc2-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="3efc2-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="3efc2-130">-SourceName</span></span>
<span data-ttu-id="3efc2-131">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="3efc2-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efc2-132">-Hedefadı</span><span class="sxs-lookup"><span data-stu-id="3efc2-132">-TargetName</span></span>
<span data-ttu-id="3efc2-133">İçeriğin yeni adı</span><span class="sxs-lookup"><span data-stu-id="3efc2-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efc2-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="3efc2-134">-Confirm</span></span>
<span data-ttu-id="3efc2-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3efc2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3efc2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3efc2-136">-WhatIf</span></span>
<span data-ttu-id="3efc2-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3efc2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3efc2-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3efc2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3efc2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3efc2-139">CommonParameters</span></span>
<span data-ttu-id="3efc2-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3efc2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3efc2-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3efc2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3efc2-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3efc2-142">INPUTS</span></span>

### <span data-ttu-id="3efc2-143">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3efc2-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="3efc2-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3efc2-144">OUTPUTS</span></span>

### <span data-ttu-id="3efc2-145">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3efc2-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="3efc2-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3efc2-146">NOTES</span></span>

## <span data-ttu-id="3efc2-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3efc2-147">RELATED LINKS</span></span>
