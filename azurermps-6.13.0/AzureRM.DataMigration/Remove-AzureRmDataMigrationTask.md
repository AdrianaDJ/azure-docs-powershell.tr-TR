---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Remove-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: 295ac647bcbe04e26e761e4fdf8fe2bd30282218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594418"
---
# <span data-ttu-id="e5ddf-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="e5ddf-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="e5ddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ddf-103">Azure 'dan Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5ddf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5ddf-104">SYNTAX</span></span>

### <span data-ttu-id="e5ddf-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5ddf-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5ddf-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="e5ddf-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5ddf-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e5ddf-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5ddf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5ddf-108">DESCRIPTION</span></span>
<span data-ttu-id="e5ddf-109">Remove-AzureRmDataMigrationTask cmdlet 'i Azure 'dan Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="e5ddf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5ddf-110">EXAMPLES</span></span>

### <span data-ttu-id="e5ddf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5ddf-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="e5ddf-112">Önceki örnek, görev adı parametresine bağlı olarak Azure 'dan TestTask adındaki bir Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="e5ddf-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e5ddf-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="e5ddf-114">Önceki örnek, gelen PSProjectTask nesnesine dayalı bir Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="e5ddf-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5ddf-115">PARAMETERS</span></span>

### <span data-ttu-id="e5ddf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ddf-116">-DefaultProfile</span></span>
<span data-ttu-id="e5ddf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ddf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e5ddf-118">-Force</span></span>
<span data-ttu-id="e5ddf-119">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="e5ddf-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e5ddf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5ddf-120">-InputObject</span></span>
<span data-ttu-id="e5ddf-121">PSProjectTask nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-121">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ddf-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5ddf-122">-Name</span></span>
<span data-ttu-id="e5ddf-123">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-123">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ddf-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e5ddf-124">-PassThru</span></span>
<span data-ttu-id="e5ddf-125">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-125">Returns an true/false.</span></span>
<span data-ttu-id="e5ddf-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e5ddf-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="e5ddf-127">-ProjectName</span></span>
<span data-ttu-id="e5ddf-128">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-128">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ddf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ddf-129">-ResourceGroupName</span></span>
<span data-ttu-id="e5ddf-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ddf-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e5ddf-131">-ResourceId</span></span>
<span data-ttu-id="e5ddf-132">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-132">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5ddf-133">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="e5ddf-133">-ServiceName</span></span>
<span data-ttu-id="e5ddf-134">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-134">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ddf-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5ddf-135">-Confirm</span></span>
<span data-ttu-id="e5ddf-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5ddf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5ddf-137">-WhatIf</span></span>
<span data-ttu-id="e5ddf-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5ddf-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5ddf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ddf-140">CommonParameters</span></span>
<span data-ttu-id="e5ddf-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5ddf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ddf-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ddf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ddf-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5ddf-143">INPUTS</span></span>

### <span data-ttu-id="e5ddf-144">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="e5ddf-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="e5ddf-145">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e5ddf-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e5ddf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e5ddf-146">System.String</span></span>

## <span data-ttu-id="e5ddf-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5ddf-147">OUTPUTS</span></span>

### <span data-ttu-id="e5ddf-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5ddf-148">System.Boolean</span></span>

## <span data-ttu-id="e5ddf-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5ddf-149">NOTES</span></span>

## <span data-ttu-id="e5ddf-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5ddf-150">RELATED LINKS</span></span>
