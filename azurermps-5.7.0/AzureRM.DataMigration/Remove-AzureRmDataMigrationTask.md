---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationTask.md
ms.openlocfilehash: d192b7f422557b4d4373f794e98cdb2556db3c63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591683"
---
# <span data-ttu-id="d849e-101">Remove-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d849e-101">Remove-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="d849e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d849e-102">SYNOPSIS</span></span>
<span data-ttu-id="d849e-103">Azure 'dan Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d849e-103">Removes an Azure Database Migration Service task from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d849e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d849e-104">SYNTAX</span></span>

### <span data-ttu-id="d849e-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d849e-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d849e-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="d849e-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-InputObject] <PSProjectTask> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d849e-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d849e-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationTask [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d849e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d849e-108">DESCRIPTION</span></span>
<span data-ttu-id="d849e-109">Remove-AzureRmDataMigrationTask cmdlet 'i Azure 'dan Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d849e-109">The Remove-AzureRmDataMigrationTask cmdlet removes an Azure Database Migration Service task from Azure.</span></span>

## <span data-ttu-id="d849e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d849e-110">EXAMPLES</span></span>

### <span data-ttu-id="d849e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d849e-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –TaskName TestTask -ProjectName myTestProject -ServiceName MyTestService
 -ResourceGroupName MyResourceGroup

```

<span data-ttu-id="d849e-112">Önceki örnek, görev adı parametresine bağlı olarak Azure 'dan TestTask adındaki bir Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d849e-112">The preceding example removes an Azure Database Migration Service task named TestTask from Azure based on task name parameter.</span></span>

### <span data-ttu-id="d849e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d849e-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationTask –InputObject $TestTask

```

<span data-ttu-id="d849e-114">Önceki örnek, gelen PSProjectTask nesnesine dayalı bir Azure veritabanı geçiş hizmeti görevini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d849e-114">The preceding example removes an Azure Database Migration Service task based on PSProjectTask object passed in.</span></span>

## <span data-ttu-id="d849e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d849e-115">PARAMETERS</span></span>

### <span data-ttu-id="d849e-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="d849e-116">-Confirm</span></span>
<span data-ttu-id="d849e-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d849e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d849e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d849e-118">-DefaultProfile</span></span>
<span data-ttu-id="d849e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d849e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d849e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d849e-120">-Force</span></span>
<span data-ttu-id="d849e-121">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="d849e-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d849e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d849e-122">-InputObject</span></span>
<span data-ttu-id="d849e-123">PSProjectTask nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d849e-123">PSProjectTask Object.</span></span>

```yaml
Type: PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d849e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="d849e-124">-Name</span></span>
<span data-ttu-id="d849e-125">Görevin adı.</span><span class="sxs-lookup"><span data-stu-id="d849e-125">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d849e-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d849e-126">-PassThru</span></span>
<span data-ttu-id="d849e-127">Bir doğru/yanlış döndürür.</span><span class="sxs-lookup"><span data-stu-id="d849e-127">Returns an true/false.</span></span>
<span data-ttu-id="d849e-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d849e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d849e-129">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="d849e-129">-ProjectName</span></span>
<span data-ttu-id="d849e-130">Projenin adı.</span><span class="sxs-lookup"><span data-stu-id="d849e-130">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d849e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d849e-131">-ResourceGroupName</span></span>
<span data-ttu-id="d849e-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d849e-132">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d849e-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d849e-133">-ResourceId</span></span>
<span data-ttu-id="d849e-134">Proje kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d849e-134">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d849e-135">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="d849e-135">-ServiceName</span></span>
<span data-ttu-id="d849e-136">Veri geçişi hizmeti adı.</span><span class="sxs-lookup"><span data-stu-id="d849e-136">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d849e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d849e-137">-WhatIf</span></span>
<span data-ttu-id="d849e-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d849e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d849e-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d849e-139">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="d849e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d849e-140">INPUTS</span></span>

### <span data-ttu-id="d849e-141">Microsoft. Azure. Commands. DataMigration. modeller. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="d849e-141">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>
<span data-ttu-id="d849e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d849e-142">System.String</span></span>


## <span data-ttu-id="d849e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d849e-143">OUTPUTS</span></span>

### <span data-ttu-id="d849e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d849e-144">System.Boolean</span></span>


## <span data-ttu-id="d849e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d849e-145">NOTES</span></span>

## <span data-ttu-id="d849e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d849e-146">RELATED LINKS</span></span>


