---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Remove-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationTask.md
ms.openlocfilehash: c5307aa4e7f78e8586ff28fd77bd125cdf736602
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274576"
---
# <span data-ttu-id="d751d-101">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d751d-101">Remove-AzDataMigrationTask</span></span>

## <span data-ttu-id="d751d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d751d-102">SYNOPSIS</span></span>
<span data-ttu-id="d751d-103">Azure 'dan Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d751d-103">Removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="d751d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d751d-104">SYNTAX</span></span>

### <span data-ttu-id="d751d-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d751d-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d751d-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="d751d-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d751d-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d751d-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d751d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d751d-108">DESCRIPTION</span></span>
<span data-ttu-id="d751d-109">Remove-AzDataMigrationTask cmdlet 'i Azure 'dan Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d751d-109">The Remove-AzDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="d751d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d751d-110">EXAMPLES</span></span>

### <span data-ttu-id="d751d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d751d-111">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationTask -TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="d751d-112">Önceki örnek, görev adı parametresine bağlı olarak Azure 'dan TestTask adındaki bir Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d751d-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="d751d-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d751d-113">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationTask -InputObject $TestTask
```

<span data-ttu-id="d751d-114">Önceki örnek, gelen PSProjectTask nesnesine dayalı bir Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d751d-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="d751d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d751d-115">PARAMETERS</span></span>

### <span data-ttu-id="d751d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d751d-116">-DefaultProfile</span></span>
<span data-ttu-id="d751d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d751d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d751d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d751d-118">-Force</span></span>
<span data-ttu-id="d751d-119">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="d751d-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d751d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d751d-120">-InputObject</span></span>
<span data-ttu-id="d751d-121">PSProjectTask nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d751d-121">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="d751d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d751d-122">-Name</span></span>
<span data-ttu-id="d751d-123">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="d751d-123">The name of the task.</span></span>

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

### <span data-ttu-id="d751d-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d751d-124">-PassThru</span></span>
<span data-ttu-id="d751d-125">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="d751d-125">Returns an true/false.</span></span>
<span data-ttu-id="d751d-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d751d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d751d-127">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="d751d-127">-ProjectName</span></span>
<span data-ttu-id="d751d-128">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="d751d-128">The name of the project.</span></span>

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

### <span data-ttu-id="d751d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d751d-129">-ResourceGroupName</span></span>
<span data-ttu-id="d751d-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d751d-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="d751d-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d751d-131">-ResourceId</span></span>
<span data-ttu-id="d751d-132">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d751d-132">Project Resource Id.</span></span>

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

### <span data-ttu-id="d751d-133">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d751d-133">-ServiceName</span></span>
<span data-ttu-id="d751d-134">Veritabanı geçiş hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="d751d-134">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="d751d-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="d751d-135">-Confirm</span></span>
<span data-ttu-id="d751d-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d751d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d751d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d751d-137">-WhatIf</span></span>
<span data-ttu-id="d751d-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d751d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d751d-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d751d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d751d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d751d-140">CommonParameters</span></span>
<span data-ttu-id="d751d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d751d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d751d-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d751d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d751d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d751d-143">INPUTS</span></span>

### <span data-ttu-id="d751d-144">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="d751d-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="d751d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d751d-145">System.String</span></span>

## <span data-ttu-id="d751d-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d751d-146">OUTPUTS</span></span>

### <span data-ttu-id="d751d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d751d-147">System.Boolean</span></span>

## <span data-ttu-id="d751d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d751d-148">NOTES</span></span>

## <span data-ttu-id="d751d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d751d-149">RELATED LINKS</span></span>
