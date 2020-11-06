---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: aea1fac4450a8625eb3d31e9f951a465344a3bd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590089"
---
# <span data-ttu-id="77cc3-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="77cc3-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="77cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="77cc3-103">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="77cc3-103">Rename an Azure context.</span></span>  <span data-ttu-id="77cc3-104">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="77cc3-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77cc3-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77cc3-105">SYNTAX</span></span>

### <span data-ttu-id="77cc3-106">RenameByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="77cc3-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="77cc3-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="77cc3-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="77cc3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="77cc3-108">DESCRIPTION</span></span>
<span data-ttu-id="77cc3-109">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="77cc3-109">Rename an Azure context.</span></span>  <span data-ttu-id="77cc3-110">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="77cc3-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="77cc3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77cc3-111">EXAMPLES</span></span>

### <span data-ttu-id="77cc3-112">Adlandırılmış parametreler kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="77cc3-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="77cc3-113">' user1@contoso.org ' ' 12345-6789-2345-3567890 ' aboneliği ile ' ' çalışma '</span><span class="sxs-lookup"><span data-stu-id="77cc3-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="77cc3-114">Bu komuttan sonra, ' Select-AzureRmContext çalışması ' kullanarak içeriği hedefleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77cc3-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="77cc3-115">Sekme tamamlamayı kullanarak ' SourceName ' değerleri arasında sekme alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="77cc3-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="77cc3-116">Konum parametrelerini kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="77cc3-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="77cc3-117">"My Context" adlı bağlamı "Iş" olarak yeniden adlandırın.</span><span class="sxs-lookup"><span data-stu-id="77cc3-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="77cc3-118">Bu komuttan sonra, Select-AzureRmContext Iş kullanarak bağlam hedefleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="77cc3-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="77cc3-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77cc3-119">PARAMETERS</span></span>

### <span data-ttu-id="77cc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cc3-120">-DefaultProfile</span></span>
<span data-ttu-id="77cc3-121">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="77cc3-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77cc3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="77cc3-122">-Force</span></span>
<span data-ttu-id="77cc3-123">Hedef bağlamı zaten var olsa bile içeriği yeniden adlandır</span><span class="sxs-lookup"><span data-stu-id="77cc3-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="77cc3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77cc3-124">-InputObject</span></span>
<span data-ttu-id="77cc3-125">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="77cc3-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77cc3-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="77cc3-126">-PassThru</span></span>
<span data-ttu-id="77cc3-127">Yeniden adlandırılan bağlamı döndür.</span><span class="sxs-lookup"><span data-stu-id="77cc3-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="77cc3-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="77cc3-128">-Scope</span></span>
<span data-ttu-id="77cc3-129">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="77cc3-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="77cc3-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="77cc3-130">-SourceName</span></span>
<span data-ttu-id="77cc3-131">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="77cc3-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77cc3-132">-Hedefadı</span><span class="sxs-lookup"><span data-stu-id="77cc3-132">-TargetName</span></span>
<span data-ttu-id="77cc3-133">İçeriğin yeni adı</span><span class="sxs-lookup"><span data-stu-id="77cc3-133">The new name of the context</span></span>

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

### <span data-ttu-id="77cc3-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="77cc3-134">-Confirm</span></span>
<span data-ttu-id="77cc3-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="77cc3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77cc3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77cc3-136">-WhatIf</span></span>
<span data-ttu-id="77cc3-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="77cc3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77cc3-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="77cc3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77cc3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cc3-139">CommonParameters</span></span>
<span data-ttu-id="77cc3-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77cc3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77cc3-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77cc3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cc3-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77cc3-142">INPUTS</span></span>

### <span data-ttu-id="77cc3-143">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="77cc3-143">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="77cc3-144">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77cc3-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="77cc3-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77cc3-145">OUTPUTS</span></span>

### <span data-ttu-id="77cc3-146">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="77cc3-146">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="77cc3-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77cc3-147">NOTES</span></span>

## <span data-ttu-id="77cc3-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77cc3-148">RELATED LINKS</span></span>
