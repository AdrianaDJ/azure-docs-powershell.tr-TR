---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764800"
---
# <span data-ttu-id="e3caa-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e3caa-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="e3caa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3caa-102">SYNOPSIS</span></span>
<span data-ttu-id="e3caa-103">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="e3caa-103">Rename an Azure context.</span></span>  <span data-ttu-id="e3caa-104">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="e3caa-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3caa-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3caa-105">SYNTAX</span></span>

### <span data-ttu-id="e3caa-106">Giriş nesnesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3caa-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="e3caa-107">Bağlam adı</span><span class="sxs-lookup"><span data-stu-id="e3caa-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="e3caa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3caa-108">DESCRIPTION</span></span>
<span data-ttu-id="e3caa-109">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="e3caa-109">Rename an Azure context.</span></span>  <span data-ttu-id="e3caa-110">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="e3caa-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="e3caa-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3caa-111">EXAMPLES</span></span>

### <span data-ttu-id="e3caa-112">Adlandırılmış parametreler kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="e3caa-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="e3caa-113">' user1@contoso.org ' ' 12345-6789-2345-3567890 ' aboneliği ile ' ' çalışma '</span><span class="sxs-lookup"><span data-stu-id="e3caa-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="e3caa-114">Bu komuttan sonra, ' Select-AzureRmContext çalışması ' kullanarak içeriği hedefleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3caa-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="e3caa-115">Sekme tamamlamayı kullanarak ' SourceName ' değerleri arasında sekme alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e3caa-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="e3caa-116">Konum parametrelerini kullanarak bağlamı yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="e3caa-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="e3caa-117">"My Context" adlı bağlamı "Iş" olarak yeniden adlandırın.</span><span class="sxs-lookup"><span data-stu-id="e3caa-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="e3caa-118">Bu komuttan sonra, Select-AzureRmContext Iş kullanarak bağlam hedefleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e3caa-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="e3caa-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3caa-119">PARAMETERS</span></span>

### <span data-ttu-id="e3caa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3caa-120">-DefaultProfile</span></span>
<span data-ttu-id="e3caa-121">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e3caa-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3caa-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e3caa-122">-Force</span></span>
<span data-ttu-id="e3caa-123">Hedef bağlamı zaten var olsa bile içeriği yeniden adlandır</span><span class="sxs-lookup"><span data-stu-id="e3caa-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="e3caa-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3caa-124">-InputObject</span></span>
<span data-ttu-id="e3caa-125">Normalde ardışık düzen aracılığıyla iletilen bir bağlam nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e3caa-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3caa-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e3caa-126">-PassThru</span></span>
<span data-ttu-id="e3caa-127">Yeniden adlandırılan bağlamı döndür.</span><span class="sxs-lookup"><span data-stu-id="e3caa-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="e3caa-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="e3caa-128">-Scope</span></span>
<span data-ttu-id="e3caa-129">Bağlam değişikliklerinin kapsamını belirler, örneğin, WHEA değişiklikleri yalnızca örnek işleme uygulanır veya bu kullanıcı tarafından başlatılan tüm oturumlar için</span><span class="sxs-lookup"><span data-stu-id="e3caa-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="e3caa-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="e3caa-130">-SourceName</span></span>
<span data-ttu-id="e3caa-131">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="e3caa-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3caa-132">-Hedefadı</span><span class="sxs-lookup"><span data-stu-id="e3caa-132">-TargetName</span></span>
<span data-ttu-id="e3caa-133">İçeriğin yeni adı</span><span class="sxs-lookup"><span data-stu-id="e3caa-133">The new name of the context</span></span>

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

### <span data-ttu-id="e3caa-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3caa-134">-Confirm</span></span>
<span data-ttu-id="e3caa-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3caa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3caa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3caa-136">-WhatIf</span></span>
<span data-ttu-id="e3caa-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3caa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3caa-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3caa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3caa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3caa-139">CommonParameters</span></span>
<span data-ttu-id="e3caa-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3caa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3caa-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3caa-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3caa-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3caa-142">INPUTS</span></span>

### <span data-ttu-id="e3caa-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e3caa-143">None</span></span>

## <span data-ttu-id="e3caa-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3caa-144">OUTPUTS</span></span>

### <span data-ttu-id="e3caa-145">Microsoft. Azure. Commands. Profile. modeller. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e3caa-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="e3caa-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3caa-146">NOTES</span></span>

## <span data-ttu-id="e3caa-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3caa-147">RELATED LINKS</span></span>

