---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276110"
---
# <span data-ttu-id="c8a92-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="c8a92-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="c8a92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8a92-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a92-103">Bir şeması dosyasını JSON biçiminde bir şeması nesnesine aktarın ve belirtilen abonelik veya yönetim grubunun içine kaydedin.</span><span class="sxs-lookup"><span data-stu-id="c8a92-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="c8a92-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8a92-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a92-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8a92-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a92-106">Bir şeması tanımını dışlayıcılarla içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="c8a92-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="c8a92-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8a92-107">EXAMPLES</span></span>

### <span data-ttu-id="c8a92-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c8a92-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="c8a92-109">Bir şeması tanımını dışlayıcılarla içeri aktarın ve bir abonelik içinde saklayın.</span><span class="sxs-lookup"><span data-stu-id="c8a92-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="c8a92-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8a92-110">PARAMETERS</span></span>

### <span data-ttu-id="c8a92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a92-111">-DefaultProfile</span></span>
<span data-ttu-id="c8a92-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8a92-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a92-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c8a92-113">-Force</span></span>
<span data-ttu-id="c8a92-114">True olarak ayarlandığında, yürütme onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="c8a92-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="c8a92-115">-Includealt klasörler</span><span class="sxs-lookup"><span data-stu-id="c8a92-115">-IncludeSubFolders</span></span>
<span data-ttu-id="c8a92-116">True olarak ayarlandığında, alt klasörlerdeki yapıt dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="c8a92-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="c8a92-117">-Inputpath</span><span class="sxs-lookup"><span data-stu-id="c8a92-117">-InputPath</span></span>
<span data-ttu-id="c8a92-118">Disk üzerindeki bir Blueprint JSON dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="c8a92-118">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a92-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c8a92-119">-ManagementGroupId</span></span>
<span data-ttu-id="c8a92-120">Şeması tanımının olduğu veya kaydedileceği yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="c8a92-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a92-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8a92-121">-Name</span></span>
<span data-ttu-id="c8a92-122">Blueprint tanım adı.</span><span class="sxs-lookup"><span data-stu-id="c8a92-122">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a92-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c8a92-123">-PassThru</span></span>
<span data-ttu-id="c8a92-124">Ayarlandığında cmdlet, içeri aktarılan şeması tanımını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="c8a92-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="c8a92-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c8a92-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8a92-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c8a92-126">-SubscriptionId</span></span>
<span data-ttu-id="c8a92-127">Şeması tanımının bulunduğu abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="c8a92-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a92-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c8a92-128">-Confirm</span></span>
<span data-ttu-id="c8a92-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c8a92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a92-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a92-130">-WhatIf</span></span>
<span data-ttu-id="c8a92-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c8a92-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8a92-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c8a92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a92-133">CommonParameters</span></span>
<span data-ttu-id="c8a92-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8a92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a92-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c8a92-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a92-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8a92-136">INPUTS</span></span>

### <span data-ttu-id="c8a92-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a92-137">System.String</span></span>

## <span data-ttu-id="c8a92-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8a92-138">OUTPUTS</span></span>

### <span data-ttu-id="c8a92-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a92-139">System.String</span></span>

## <span data-ttu-id="c8a92-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8a92-140">NOTES</span></span>

## <span data-ttu-id="c8a92-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8a92-141">RELATED LINKS</span></span>
