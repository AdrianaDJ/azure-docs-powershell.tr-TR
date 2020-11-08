---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 00f9b84c1e3e8a5bb9a506952cce9ab45e55b9e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935236"
---
# <span data-ttu-id="418cd-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="418cd-101">Rename-AzContext</span></span>

## <span data-ttu-id="418cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="418cd-102">SYNOPSIS</span></span>
<span data-ttu-id="418cd-103">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="418cd-103">Rename an Azure context.</span></span>  <span data-ttu-id="418cd-104">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="418cd-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="418cd-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="418cd-105">SYNTAX</span></span>

### <span data-ttu-id="418cd-106">RenameByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="418cd-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="418cd-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="418cd-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="418cd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="418cd-108">DESCRIPTION</span></span>
<span data-ttu-id="418cd-109">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="418cd-109">Rename an Azure context.</span></span>  <span data-ttu-id="418cd-110">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="418cd-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="418cd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="418cd-111">EXAMPLES</span></span>

### <span data-ttu-id="418cd-112">Adlandırılmış parametreler kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="418cd-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="418cd-113">' user1@contoso.org ' ' 12345-6789-2345-3567890 ' aboneliği ile ' ' çalışma '</span><span class="sxs-lookup"><span data-stu-id="418cd-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="418cd-114">Bu komuttan sonra, ' Select-AzContext çalışması ' kullanarak bağlamı hedefleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418cd-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="418cd-115">Sekme tamamlamayı kullanarak ' SourceName ' değerleri arasında sekme alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418cd-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="418cd-116">Konum parametrelerini kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="418cd-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="418cd-117">"My Context" adlı bağlamı "Iş" olarak yeniden adlandırın.</span><span class="sxs-lookup"><span data-stu-id="418cd-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="418cd-118">Bu komuttan sonra, Select-AzContext Iş kullanarak bağlam hedefleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="418cd-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="418cd-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="418cd-119">PARAMETERS</span></span>

### <span data-ttu-id="418cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418cd-120">-DefaultProfile</span></span>
<span data-ttu-id="418cd-121">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="418cd-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="418cd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="418cd-122">-Force</span></span>
<span data-ttu-id="418cd-123">Hedef bağlamı zaten var olsa bile içeriği yeniden adlandır</span><span class="sxs-lookup"><span data-stu-id="418cd-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="418cd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="418cd-124">-InputObject</span></span>
<span data-ttu-id="418cd-125">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="418cd-125">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="418cd-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="418cd-126">-PassThru</span></span>
<span data-ttu-id="418cd-127">Yeniden adlandırılan bağlamı döndür.</span><span class="sxs-lookup"><span data-stu-id="418cd-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="418cd-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="418cd-128">-Scope</span></span>
<span data-ttu-id="418cd-129">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="418cd-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="418cd-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="418cd-130">-SourceName</span></span>
<span data-ttu-id="418cd-131">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="418cd-131">The name of the context</span></span>

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

### <span data-ttu-id="418cd-132">-Hedefadı</span><span class="sxs-lookup"><span data-stu-id="418cd-132">-TargetName</span></span>
<span data-ttu-id="418cd-133">İçeriğin yeni adı</span><span class="sxs-lookup"><span data-stu-id="418cd-133">The new name of the context</span></span>

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

### <span data-ttu-id="418cd-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="418cd-134">-Confirm</span></span>
<span data-ttu-id="418cd-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="418cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="418cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418cd-136">-WhatIf</span></span>
<span data-ttu-id="418cd-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="418cd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="418cd-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="418cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="418cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418cd-139">CommonParameters</span></span>
<span data-ttu-id="418cd-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="418cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418cd-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="418cd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418cd-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="418cd-142">INPUTS</span></span>

### <span data-ttu-id="418cd-143">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="418cd-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="418cd-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="418cd-144">OUTPUTS</span></span>

### <span data-ttu-id="418cd-145">Microsoft. Azure. Commands. Profile. modeller. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="418cd-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="418cd-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="418cd-146">NOTES</span></span>

## <span data-ttu-id="418cd-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="418cd-147">RELATED LINKS</span></span>