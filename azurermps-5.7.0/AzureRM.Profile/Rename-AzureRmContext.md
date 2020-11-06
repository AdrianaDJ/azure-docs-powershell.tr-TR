---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 6163602d2975a9ec77e572ec0033ef2c626d2cfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592435"
---
# <span data-ttu-id="edcdd-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="edcdd-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="edcdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edcdd-102">SYNOPSIS</span></span>
<span data-ttu-id="edcdd-103">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="edcdd-103">Rename an Azure context.</span></span>  <span data-ttu-id="edcdd-104">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="edcdd-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edcdd-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edcdd-105">SYNTAX</span></span>

### <span data-ttu-id="edcdd-106">RenameByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="edcdd-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="edcdd-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="edcdd-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="edcdd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="edcdd-108">DESCRIPTION</span></span>
<span data-ttu-id="edcdd-109">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="edcdd-109">Rename an Azure context.</span></span>  <span data-ttu-id="edcdd-110">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="edcdd-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="edcdd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edcdd-111">EXAMPLES</span></span>

### <span data-ttu-id="edcdd-112">Adlandırılmış parametreler kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="edcdd-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="edcdd-113">' user1@contoso.org ' ' 12345-6789-2345-3567890 ' aboneliği ile ' ' çalışma '</span><span class="sxs-lookup"><span data-stu-id="edcdd-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="edcdd-114">Bu komuttan sonra, ' Select-AzureRmContext çalışması ' kullanarak içeriği hedefleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="edcdd-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="edcdd-115">Sekme tamamlamayı kullanarak ' SourceName ' değerleri arasında sekme alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="edcdd-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="edcdd-116">Konum parametrelerini kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="edcdd-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="edcdd-117">"My Context" adlı bağlamı "Iş" olarak yeniden adlandırın.</span><span class="sxs-lookup"><span data-stu-id="edcdd-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="edcdd-118">Bu komuttan sonra, Select-AzureRmContext Iş kullanarak bağlam hedefleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="edcdd-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="edcdd-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edcdd-119">PARAMETERS</span></span>

### <span data-ttu-id="edcdd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edcdd-120">-DefaultProfile</span></span>
<span data-ttu-id="edcdd-121">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="edcdd-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="edcdd-122">-Force</span></span>
<span data-ttu-id="edcdd-123">Hedef bağlamı zaten var olsa bile içeriği yeniden adlandır</span><span class="sxs-lookup"><span data-stu-id="edcdd-123">Rename the context even if the target context already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edcdd-124">-InputObject</span></span>
<span data-ttu-id="edcdd-125">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="edcdd-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RenameByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="edcdd-126">-PassThru</span></span>
<span data-ttu-id="edcdd-127">Yeniden adlandırılan bağlamı döndür.</span><span class="sxs-lookup"><span data-stu-id="edcdd-127">Return the renamed context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="edcdd-128">-Scope</span></span>
<span data-ttu-id="edcdd-129">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler</span><span class="sxs-lookup"><span data-stu-id="edcdd-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="edcdd-130">-SourceName</span></span>
<span data-ttu-id="edcdd-131">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="edcdd-131">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RenameByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-132">-Hedefadı</span><span class="sxs-lookup"><span data-stu-id="edcdd-132">-TargetName</span></span>
<span data-ttu-id="edcdd-133">İçeriğin yeni adı</span><span class="sxs-lookup"><span data-stu-id="edcdd-133">The new name of the context</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="edcdd-134">-Confirm</span></span>
<span data-ttu-id="edcdd-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edcdd-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edcdd-136">-WhatIf</span></span>
<span data-ttu-id="edcdd-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edcdd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edcdd-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edcdd-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edcdd-139">CommonParameters</span></span>
<span data-ttu-id="edcdd-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edcdd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edcdd-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edcdd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edcdd-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edcdd-142">INPUTS</span></span>

### <span data-ttu-id="edcdd-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="edcdd-143">None</span></span>

## <span data-ttu-id="edcdd-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edcdd-144">OUTPUTS</span></span>

### <span data-ttu-id="edcdd-145">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="edcdd-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="edcdd-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edcdd-146">NOTES</span></span>

## <span data-ttu-id="edcdd-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edcdd-147">RELATED LINKS</span></span>

